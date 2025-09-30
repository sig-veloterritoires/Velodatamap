Fonctionnalités générales
=========================

.. _Fonctionnalités générales:

.. |cartes| image:: images/icons/cartes.png
            :width: 30

.. |couches| image:: images/icons/couches.png
            :width: 30

.. |rechercher| image:: images/icons/rechercher.png
            :width: 30

.. |filtrer| image:: images/icons/filtrer.png
            :width: 30

.. |connecte| image:: images/icons/connecte.png
            :width: 30

.. |ajout_entite| image:: images/icons/ajout_entite.png
            :width: 30

.. |modifier| image:: images/icons/modifier.png
            :height: 30

.. |enregistrer| image:: images/icons/enregistrer.png
            :height: 30

.. |requeteur| image:: images/icons/requeteur.png
            :width: 30

.. |extraction| image:: images/icons/extraction.png

.. |telechargement_tabulaire| image:: images/icons/telechargement_tabulaire.png
            :width: 30

.. |comparer| image:: images/icons/comparer.png
            :width: 30

.. |mesurer| image:: images/icons/mesurer.png
            :width: 30

.. |selection_par_geometrie| image:: images/selection_par_geometrie.png


Les principales fonctionnalités de Velodatamap, utiles dans plusieurs des cartes disponibles, sont résumées sur l'image ci-dessous, et chacune d'entre elle est présentée via une image animée (GIF) plus bas.

.. figure:: images/resume_fonctionnalites.png
   :width: 100%

.. note::
   Si les GIFs qui suivent sont trop petits pour vous, n'hésitez pas à les agrandir avec un clic-droit et l'option « Ouvrir l'image dans un nouvel onglet »

.. dropdown:: Circuler entre les cartes
   :animate: fade-in-slide-down

   Velodatamap a quatre cartes principales : **Véloroutes**, **Équipements**, **Signalement** et **Aménagements**.
   Vous pouvez circuler entre les différentes cartes en cliquant sur l'icône |cartes| puis en cliquant sur l'une d'entre elles :

   .. figure:: images/gifs/cartes.gif


.. dropdown:: Activer les différentes couches de données
   :animate: fade-in-slide-down

   Différentes couches de données peuvent être affichées sur chaque carte. Certaines s'affichent par défaut dès le chargement, et d'autres sont désactivées par défaut mais peuvent vous être utiles !
   Cliquez sur |couches| pour accéder à l'interface suivante :

   .. figure:: images/gifs/couches.gif


.. dropdown:: Afficher la légende
   :animate: fade-in-slide-down

   Besoin de comprendre les données qui s'affichent sur la carte ? Affichez la légende propre à chaque carte, toujours en cliquant sur |couches| :

   .. figure:: images/gifs/legende.gif


.. dropdown:: Faire une recherche parmi les données
   :animate: fade-in-slide-down

   Besoin de chercher une donnée en particulier ? Utilisez le bouton |rechercher| pour accéder à l'interface suivante :

   .. figure:: images/gifs/rechercher.gif


.. dropdown:: Filtrer graphiquement les données
   :animate: fade-in-slide-down

   Si vous souhaitez n'afficher que certaines données d'une couche, alors cliquez sur le bouton |filtrer| et suivez la démarche ci-dessous. Si vous souhaitez télécharger le résultat de votre filtre, celui-ci sera actif automatiquement dans le requêteur à son ouverture. Le cas échéant, n'oubliez pas de sélectionner l'option « Filtre en cours » !  Vous pouvez combiner plusieurs filtres sur des champs différents, en choisissant comme opérateur général ``Et`` ou ``Ou``.

   Pour filtrer sur les valeurs d'un champ, par exemple ``statut``, vous avez le choix entre plusieurs opérateurs de comparaison. Ces opérateurs comparent la valeur du champ filtré pour chaque donnée à la valeur que vous renseignez dans le filtre. Les opérateurs disponibles dépendent du type du champ.
   
   Les opérateurs suivants sont disponibles quel que soit le type du champ filtré :

   - ``Existe`` renvoie les données pour lesquelles le champ filtré a une valeur. Exemple de données renvoyées pour le filtre ``statut Existe`` : données pour lesquelles ``statut = "Halte-repos"``
   - ``N'existe pas`` renvoie les données pour lesquelles le champ filtré n'a pas de valeur. Exemple de données renvoyées pour le filtre ``statut N'existe pas`` : données pour lesquelles ``statut = null``

   Les opérateurs suivants sont disponibles pour les champs de type textuel :
   
   - ``=`` renvoie les données pour lesquelles le champ filtré est strictement égal à la valeur de filtre. Exemple de données renvoyées pour le filtre ``statut = "Halte-repos"`` : données pour lesquelles ``statut = "Halte-repos"`` 
   - ``~`` renvoie les données pour lesquelles le champ filtré contient la valeur renseignée de filtre. Équivalent de l'opérateur SQL ``ILIKE``. Exemple de données renvoyées pour le filtre ``statut ~ halte-r`` : données pour lesquelles ``statut = "Halte-repos"``
   - ``!=`` renvoie les données pour lesquelles le champ filtré n'est pas égal à la valeur renseignée de filtre. Exemple de données renvoyées pour le filtre ``statut != Halte-vélo`` : données pour lesquelles ``statut = "Halte-repos"``

   Les opérateurs suivants sont disponibles pour les champs de type booléen (Vrai/Faux) :

   - ``Est vrai`` renvoie les données pour lesquelles le champ filtré a la valeur booléenne "true". Exemple de données renvoyées pour le filtre ``photo Est vrai`` : ``photo = true``
   - ``Est faux`` renvoie les données pour lesquelles le champ filtré a la valeur booléenne "false". Exemple de données renvoyées pour le filtre ``photo Est faux`` : ``photo = false``

   Les opérateurs suivants sont disponibles pour les champs de type numérique ou date :

   - ``=`` renvoie les données pour lesquelles le champ filtré est strictement égal à la valeur de filtre. Exemple de données renvoyées pour le filtre ``nombre_equip = 5`` : données pour lesquelles ``nombre_equip = 5``
   - ``!=`` renvoie les données pour lesquelles le champ filtré n'est pas égal à la valeur renseignée de filtre. Exemple de données renvoyées pour le filtre ``nombre_equip != 4`` : données pour lesquelles ``nombre_equip = 5``
   - ``<`` renvoie les données pour lesquelles le champ filtré est inférieur à la valeur de filtre. Exemple de données renvoyées pour le filtre ``nombre_equip < 6`` : données pour lesquelles ``nombre_equip = 5``
   - ``<=`` renvoie les données pour lesquelles le champ filtré est inférieur ou égal à la valeur renseignée de filtre. Exemple de données renvoyées pour le filtre ``nombre_equip <= 5`` : données pour lesquelles ``nombre_equip = 5``
   - ``>`` renvoie les données pour lesquelles le champ filtré est supérieur à la valeur de filtre. Exemple de données renvoyées pour le filtre ``nombre_equip > 4`` : données pour lesquelles ``nombre_equip = 5``
   - ``>=`` renvoie les données pour lesquelles le champ filtré est supérieur ou égal à la valeur renseignée de filtre. Exemple de données renvoyées pour le filtre ``nombre_equip >= 5`` : données pour lesquelles ``nombre_equip = 5``

   .. figure:: images/gifs/filtrer.gif


.. dropdown:: Sélectionner des données par géométrie
   :animate: fade-in-slide-down

   Vous pouvez créer une sélection de données pour affichage et téléchargement dans le requêteur avec des formes géométriques. Pour cela, il suffit de cliquer sur |ajout_entite|, et de choisir une option de sélection par géométrie |selection_par_geometrie|. Tracez ensuite une forme sur la carte, et les entités l'intersectant s'afficheront automatiquement dans le requêteur, pour consultation et téléchargement.

   .. figure:: images/gifs/selection_par_geometrie.gif


.. dropdown:: Créer une entité
   :animate: fade-in-slide-down

   Pour créer une entité, que ce soit un signalement, un équipement ou un regroupement, assurez-vous d'être connecté·e, ce qui est le cas si l'icône en haut à droite est |connecte|. Cliquez ensuite sur |ajout_entite| et laissez-vous guider par l'animation suivante :

   .. figure:: images/gifs/ajout_entite.gif


.. dropdown:: Modifier une entité
   :animate: fade-in-slide-down

   Pour modifier une entité, assurez-vous d'être connecté·e, ce qui est le cas si l'icône en haut à droite est |connecte|. Sélectionnez ensuite l'entité que vous souhaitez modifier en cliquant dessus, appuyez sur |modifier| et n'oubliez pas de |enregistrer| : 

   .. figure:: images/gifs/selectionner_et_modifier.gif


.. dropdown:: Télécharger des données
   :animate: fade-in-slide-down

   Toutes les données téléchargeables des cartes véloroutes et équipements sont utilisables sous les conditions de la licence `Open Data Commons Open Database License v1.0 <https://opendatacommons.org/licenses/odbl/summary/>`_. L'attribution « Les collectivités contributrices de l'Observatoire national des véloroutes. Réseau vélo et marche. » est obligatoire. 
   
   Pour accéder à l'interface de téléchargement, le requêteur, cliquez sur |requeteur|. Téléchargez des fichiers géolocalisés au format de votre choix en cliquant sur le bouton |extraction| ; ils comprendront tous les attributs nécessaires à une bonne exploitation de la donnée. Si vous n'avez besoin que d'un fichier tabulaire ne comprenant que les colonnes s'affichant dans le requêteur, vous pouvez directement cliquer sur |telechargement_tabulaire|.
   
   N'hésitez pas à utiliser et combiner les filtres qui vous permettront de n'obtenir que les données dont vous avez réellement besoin. Pour filtrer sur les valeurs d'un champ, par exemple ``commune``, vous avez le choix entre plusieurs opérateurs de comparaison. Ces opérateurs comparent la valeur du champ filtré pour chaque donnée à la valeur que vous renseignez dans le filtre. Les opérateurs disponibles sont :

   - ``~`` renvoie les données pour lesquelles le champ filtré contient la valeur renseignée de filtre. Équivalent de l'opérateur SQL ``ILIKE``. Exemple de données renvoyées pour le filtre ``commune ~ lyon`` : données pour lesquelles ``commune = Sainte-Foy-lès-Lyon``
   - ``=`` renvoie les données pour lesquelles le champ filtré est strictement égal à la valeur de filtre. Exemple de données renvoyées pour le filtre  ``commune = Sainte-Foy-lès-Lyon`` : données pour lesquelles ``commune = Sainte-Foy-lès-Lyon``
   - ``est parmi`` renvoie les données pour lesquelles le champ filtré est comprise dans la sélection de valeurs que vous renseignerez. Équivalent de l'opérateur SQL ``IN``. Exemple de données renvoyées pour le filtre ``commune est parmi Sainte-Foy-lès-Lyon, Lyon, Paris`` : données pour lesquelles ``commune = Sainte-Foy-lès-Lyon``
   - ``est vide`` renvoie les données pour lesquelles le champ filtré n'a pas de valeur. Exemple de données renvoyées pour le filtre  ``commune est vide`` : données pour lesquelles ``commune = null``
   - ``n'est pas vide`` renvoie les données pour lesquelles le champ filtré a une valeur. Exemple de données renvoyées pour le filtre  ``commune n'est pas vide`` : données pour lesquelles ``commune = Sainte-Foy-lès-Lyon``

   Une fois la demande formulée, vous recevrez un mail à l'adresse renseignée contenant un lien de téléchargement de votre fichier. Le traitement de votre demande peut prendre plusieurs minutes. Vérifiez dans vos indésirables.

   .. figure:: images/gifs/telecharger.gif


.. dropdown:: Visualiser des données externes
   :animate: fade-in-slide-down

   Vous pouvez visualiser des fichiers externes en les glissant-déposant dans l'interface de Velodatamap depuis votre explorateur de fichiers. Les formats de fichiers compatibles sont GeoJSON, Shapefile, GPX, TopoJSON et KML. Les géométries seront affichées sur la carte mais ne seront pas cliquables. Aucune information attributaire ne sera consultable. Vous pouvez importer plusieurs fichiers dans l'interface, et gérer leur visibilité et transparence dans l'onglet des couches en haut à gauche (si celui-ci est disponible). Tous les fichiers ainsi déposés sont stockés dans la mémoire locale de votre navigateur : Réseau vélo et marche n'en aura pas connaissance, et les couches ainsi créées disparaîtront à la fermeture de la page.

   .. figure:: images/gifs/visualiser_donnees_externes.gif


.. dropdown:: Comparer des cartes
   :animate: fade-in-slide-down

   Pour comparer différentes cartes entre elles, il suffit de cliquer sur |comparer| et de choisir la carte avec laquelle vous souhaitez comparer votre carte actuelle. Le zoom des deux cartes est ajusté automatiquement pour rester identique. Vous ne pourrez pas sélectionner et interroger les entités de la carte de droite.

   .. figure:: images/gifs/comparer.gif


.. dropdown:: Mesurer des distances
   :animate: fade-in-slide-down

   Mesurer des distances peut être utile, par exemple pour estimer le périmètre d'un regroupement d'équipements avant de l'implanter sur la carte. Le bouton |mesurer| est tout en bas à droite de l'écran.
   
   .. figure:: images/gifs/mesurer.gif
