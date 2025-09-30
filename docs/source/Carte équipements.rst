Carte équipements
=================

.. |ajouter| image:: images/icons/ajouter.png
            :height: 30

.. |modifier| image:: images/icons/modifier.png
            :height: 30

.. |ajouter_datatable| image:: images/icons/ajouter_datatable.png
            :height: 30

Cette carte vous permet de visualiser, gérer et télécharger les données sur les équipements vélo, halte-repos et aires de services de votre collectivité.
Vélo & Territoires a participé à la création d'un `référentiel <https://www.velo-territoires.org/politiques-cyclables/data-velo-modeles-donnees/referentiel-donnees-equipements-velo/>`_ visant à harmoniser le recensement et la description de ces infrastructures essentielles au séjour des cyclistes.

Nous proposons une implémentation de ce référentiel dans Velodatamap, s'appuyant sur la fiche-action n°8 `Équipements, aires de services et haltes repos <https://www.velo-territoires.org/ressources/categorie/publications-velo-territoires/?resource-id=8009#resource-fiche-action-n8-actualisee-equipements-aires-de-services-haltes-repos>`_, produite en janvier 2022. Un **webinaire** de présentation de cette carte s'est tenu en octobre 2024, dont vous pouvez visionner l'enregistrement `ici <https://www.velo-territoires.org/ressources/videotheque/numeriser-et-valoriser-les-equipements-haltes-repos-et-aires-de-services-le-long-des-veloroutes/>`_.

La carte « Équipements » a trois utilités principales :

- **visualiser** les équipements et regroupements d'équipements le long des véloroutes françaises (accessible sans compte) ;
- **ajouter** des données pour permettre leur diffusion ou planifier une politique d'implantation d'équipements (nécessite un compte attribué aux collectivités territoriales si besoin) ;
- **diffuser** les données via du téléchargement ponctuel (accessible sans compte) ou directement auprès de partenaires sélectionnés (France Vélo Tourisme, etc.)

Structure des données
---------------------

Il n'y a que deux types de données décrites par le référentiel : les équipements et les regroupements.
**Un équipement est une infrastructure matérielle** telle qu'un point d'eau potable, une table de pique-nique ou un point de stationnement. **Un regroupement est un ensemble cohérent d'équipements**, dont la composition définit sa catégorie : aire de services ou halte-repos.
Les équipements et les regroupements ont des géométries ponctuelles.

La méthode de classification des regroupements est la suivante :

.. _tableau:

.. figure:: images/tableau_classification_regroupements.png
   :width: 600



Bonnes pratiques
----------------

Les équipements comme les regroupements ne doivent pas se situer à plus de 3 kilomètres à vélo d'une véloroute.

Un regroupement ne doit comprendre que des équipements se situant dans un rayon de 50 mètres de sa localisation.


Données complémentaires
-----------------------

Afin d'aider à la visualisation et la planification, d'autres données que les équipements et les regroupements sont présentes sur la carte :

- Couche ``Regroupement`` : cercle de 50 mètres de rayon autour de la localisation des regroupements. Permet d'évaluer le respect de la bonne pratique associée.
- ``Véloroute avec équipements`` : véloroutes sur le tracé desquelles des équipements ont été numérisés.
- ``Véloroute (iso 3 km)`` : zones à moins de 3 kilomètres à pied des véloroutes de la couche ``Véloroute avec équipements``. Permet d'évaluer le respect de la bonne pratique associée.
- ``Véloroute autre`` : permet de visualiser le tracé des autres véloroutes de l'Observatoire national des véloroutes (couche désactivée par défaut).
- ``Limites administratives`` : permet d'afficher les limites administratives françaises, niveau de précision variant selon le zoom (couche de l'IGN, désactivée par défaut).


Interroger des données
----------------------

Pour savoir comment interroger, filtrer ou télécharger les données, lisez la page des :ref:`Fonctionnalités générales`.


Créer et modifier des équipements et regroupements
--------------------------------------------------

Les équipements et regroupements ne peuvent être créés qu'à moins de 3 kilomètres d'une véloroute "activée", soit une véloroute visible par défaut sur la carte « Équipements », dans la couche ``Véloroute avec équipements``. Si vous souhaitez qu'une véloroute supplémentaire soit activée pour lui associer des données équipements, merci de nous contacter en précisant le volume et le périmètre de ces données.

Équipements
^^^^^^^^^^^

Le formulaire de création d'un équipement n'a qu'un seul champ obligatoire, le type d'équipement. Une fois celui-ci renseigné, certains champs complémentaires peuvent apparaître. N'oubliez pas de placer l'équipement sur la carte, en zoomant au maximum pour avoir de la précision. Une fois cela fait, il suffit de cliquer sur |ajouter| pour créer l'équipement.

Lorsqu'un équipement est créé à moins de 50 mètres d'un regroupement (soit dans le cercle représentant ce dernier), il lui est automatiquement associé. **Un équipement ne peut être associé qu'à un seul regroupement**, il sera donc associé au plus proche s'il se trouve dans le périmètre de plusieurs regroupements. Cette association automatique ne se fait qu'à la création d'un équipement, et jamais à sa modification.

.. dropdown:: Lancer l'animation « Créer un équipement »
   :animate: fade-in-slide-down
   
   .. figure:: images/gifs/creation_equipement.gif


Pour modifier un équipement, il suffit de cliquer sur son icône, et ensuite sur |modifier|. Tous les champs sont modifiables, et le regroupement associé peut également être changé.

Regroupements
^^^^^^^^^^^^^

Le formulaire de création d'un regroupement n'a qu'un seul champ obligatoire à renseigner : ``Statut``. Celui-ci peut avoir trois valeurs : ``Existant``, ``En projet`` et ``Préconisé``. **Si le regroupement est qualifié d'existant**, il est impossible de lui attribuer une importance (``Halte-repos`` ou ``Aire des services``), et un algorithme se charge d'évaluer son appartenance à l'une ou l'autre des catégories, voire à aucune. **Si le regroupement est qualifié de projet ou préconisé**, alors il est possible de définir son importance, car c'est une information qui reste théorique. N'oubliez pas de placer le regroupement sur la carte, en zoomant au maximum pour avoir de la précision. Une fois cela fait, il suffit de cliquer sur |ajouter| pour créer le regroupement.

Lorsqu'un regroupement est créé, tous les équipements situés à moins de 50 mètres de celui-ci lui sont associés s'ils ne le sont pas déjà à un autre. Cette association automatique ne se fait qu'à la création d'un regroupement, et jamais à sa modification.

Pour se voir attribuer une des catégories d'importance, **un regroupement doit non seulement s'être vu associer tous les types d'équipement obligatoires** décrits dans le tableau_ de classification, **mais aussi comprendre 75 % ou plus de ces équipements dans son périmètre de 50 mètres**. Ainsi, pour se voir classer en halte-repos, un regroupement doit comprendre les deux équipements obligatoires dans son périmètre. Pour se voir classer en aire de services, trois équipements sur les quatre obligatoires présents dans le périmètre suffisent. Ceci permet une certaine flexibilité aux gestionnaires, avec un des quatre équipements obligatoires pouvant être à plus de 50 mètres du centre du regroupement.

.. dropdown:: Lancer l'animation « Créer un regroupement »
   :animate: fade-in-slide-down
   
   .. figure:: images/gifs/creation_regroupement.gif


Pour modifier un regroupement, il suffit de cliquer sur son icône, et ensuite sur |modifier|. Tous les champs sont modifiables. Les équipements associés sont dissociables via l'onglet ``Équipements associés``, et on peut associer d'autres équipements via le même tableau et le bouton |ajouter_datatable|.

Lorsqu'un regroupement est créé, il se voit associer toutes les véloroutes de l'Observatoire national se trouvant à moins de 3 kilomètres. Cette association est essentielle pour la diffusion vers les outils de partenaires comme France Vélo Tourisme. Elle permet d'afficher chaque regroupement sur ses itinéraires associés, et pas sur les autres. Pour qu'un regroupement soit pris en compte par France Vélo Tourisme, il faut que son statut soit ``Existant`` et son importance ``Aire de services`` ou ``Halte-repos``.



.. note::
    Vous venez de finaliser un recensement des équipements sur votre territoire, et souhaitez les intégrer à Velodatamap ? Le Réseau vélo et marche se charge de l'intégration de votre premier jeu de données ! Vous trouverez un gabarit de type tableur en téléchargeant le dictionnaire du `référentiel <https://www.velo-territoires.org/politiques-cyclables/data-velo-modeles-donnees/referentiel-donnees-equipements-velo/>`_ sur notre site. Contactez-nous afin d'en savoir plus.
    
    

.. note::
    Le requêteur vous permet de télécharger les équipements et les regroupements. Choisissez votre donnée en cliquant sur le bon onglet :
    
    .. figure:: images/onglets_requeteur_equipements.png
       :width: 600
