Évolutions de Velodatamap
=========================

.. note::
    Cette page présente les évolutions de Velodatamap depuis juillet 2024, vous montrant la liste des nouvelles fonctionnalités disponibles sur l'application ainsi que le travail parfois invisible de l'équipe SIG du Réseau vélo et marche.

Juin 2025
--------------
**Général :**

* Ajout de l'attribution obligatoire à l'interface de téléchargement des données, ainsi qu'à l'archive obtenue après téléchargement des données.

**Observatoire national des véloroutes :**

* Correction de l'ordre d'affichage des véloroutes en donnant la priorité aux EuroVelo puis au SNV, puis aux SRV, puis aux SDV


Mai 2025
--------------
**Signalement :**

* Ajout d'indicateurs sur les signalements (visibles dans le requêteur) ainsi que d'une fonctionnalité de génération d'un rapport Excel
* Rétablissement de la passerelle avec Suricate

**Observatoire national des véloroutes :**

* Ajout de la liste des portions et liaisons associées à chaque véloroute dans les fiches descriptives de la couche ``Véloroute``
* Ajout de la liste des segments empruntés par et des liaisons associées à chaque portion dans les fiches descriptives de la couche ``Portion de véloroute``
* Ajout de la liste des véloroutes et portions empruntant chaque segment dans les fiches descriptives de la couche ``Segment de véloroute``

Avril 2025
--------------
**Général :**

* Ajout du module « Tableau » à Velodatamap, qui permet de visualiser plus facilement des données tabulaires sans géométrie. Le module est accessible en cliquant sur le logo de l'association tout en haut à gauche de l'écran
* Les utilisateurs connectés n'ont plus besoin de renseigner leur adresse mail pour télécharger des données
* Le filtre par collectivité fonctionne indifféremment avec le nom et/ou le code INSEE sur les couches segments, équipements et regroupements

**Tableau :**

* Ajout de tables présentant des chiffres clefs sur les véloroutes traversant chaque collectivité française : longueur totale, longueur de véloroute réalisée l'année n-1, longueur de véloroute en site propre, etc. 

**Équipements :**

* Ajout de la liste des véloroutes situées à moins de 3 km d'un équipement ou regroupement dans le requêteur et l'outil de filtre

Mars 2025
--------------
**Général :**

* Les téléchargements aux formats GeoJSON et KML ne sont désormais possibles que dans le SCR WGS 84 (EPSG : 4326) afin de respecter les spécifications officielles de ces formats

**Observatoire national des véloroutes :**

* Mise en ligne des données de La Réunion


Décembre 2024
--------------
**Général :**

* Ajout du format GeoPackage à la liste des formats disponibles pour export
* Amélioration du contenu et du nommage des fichiers obtenus par la procédure d'export
* Ajout d'un fichier `ODbL_LICENSE.txt` contenant le texte de la licence associée aux données exportées à chaque export

**Équipements :**

* Les photos ajoutées à des regroupements ne peuvent plus avoir un nom dépassant 60 caractères (extension du fichier comprise)
* La couche ``Véloroutes (isodistance 3km)`` est mise à jour quotidiennement en prenant en compte les dernières modifications de tracés des véloroutes concernées

Novembre 2024
--------------
**Observatoire national des véloroutes :**

* Refonte graphique :

    * remplacement de la carte "Véloroutes" par trois cartes "Avancement", "Infrastructure" et "Niveau de schéma", mettant chacune en valeur les mêmes données de l'ONV, mais avec un point de vue différent

* Davantage de couches disponibles :
    * Monuments nationaux
    * Les Plus Beaux Villages de France

**Équipements :**

* Un équipement ne peut désormais plus être associé à un regroupement se trouvant à plus de 500 mètres de lui
* Les photos ajoutées à des équipements ne peuvent plus avoir un nom dépassant 60 caractères (extension du fichier comprise)

Octobre 2024
--------------
**Observatoire national des véloroutes :**

* Refonte graphique :

    * Remplacement de l'ancienne couche segment par 3 nouvelles (avancement, infrastructure et schéma)
    * ajout de la couche portion
    * ajout de la couche itinéraire
    * ajout de la couche liaison

* Davantage de couches disponibles :
    * limites administratives IGN
    * Plan IGN
    * Photographie aérienne IGN

* Optimisation des performances graphiques
* Création d'un nouveau champ ``numéro et nom`` plus fonctionnel sur l'ensemble des couches
* Liaisons cyclables désormais disponibles en téléchargement

Septembre 2024
--------------

**Général :**

* Changement de l'icône de téléchargement de données tabulaires dans le requêteur

**Signalement :**

* Le mail est désormais renseigné automatiquement à l'ajout d'un signalement si l'utilisateur est connecté
* Pour les catégories « Chaussée » et « Travaux », les maîtres d'ouvrage peuvent maintenant définir une date de début et de fin de validité d'un signalement. Le signalement sera automatiquement archivé le lendemain de sa date de fin de validité
* Seules les véloroutes traversant le territoire de restriction de l'utilisateur connecté sont désormais affichées (simplification visuelle, gain de performances)
* Les champs ``suivistatut`` et ``enquete`` ne sont plus affichés dans le formulaire d'insertion pour les utilisateurs connectés
* Les champs ``remarque_mo`` et ``document_complementaire``  ne sont plus affichés dans le formulaire d'insertion pour les utilisateurs non connectés
* Le statut par défaut d'un signalement créé par un utilisateur connecté est désormais « En cours de résolution ». Ce statut est modifiable en « Signalé » ou « Pris en compte » dès le formulaire de création si besoin

Août 2024
---------

**Équipements :**

* Une couche ``Véloroutes (isodistance 3km)`` est ajoutée, qui représente les zones situées à moins de 3 km à pied de chaque véloroute. Cela permet de visualiser la recommandation de la fiche-action n°8 de Vélo & Territoires, qui précise qu'une halte-repos ou une aire de services ne doit pas être à plus de 3 km à vélo d'une véloroute
* Seules les véloroutes traversant le territoire de restriction de l'utilisateur connecté sont désormais affichées (simplification visuelle, gain de performances)
* La liste des équipements manquant à un regroupement pour accéder au niveau « Aire de services » est affichée dans sa fiche descriptive
* Il est désormais impossible de créer un équipement ou un regroupement à plus de 3 km d'une véloroute "activée", c'est-à-dire qui s'affiche dans la couche ``Véloroute avec équipements``

Juillet 2024
------------

**Général :**

* Amélioration des performances de l'application
* Implémentation de la charte graphique de l'association (logos, couleurs)
* Pour les utilisateurs ayant une restriction géographique : attribution d'un zoom automatique sur le territoire ou l'itinéraire concerné par la restriction
* Changement de plusieurs icônes et attribution de couleurs aux boutons les plus utiles (connexion, ajout d'entité...)



**Équipements :**

* Refonte totale de la structure de la base de données
* Refonte graphique :

    * affichage des périmètres des regroupements et itinéraires
    * icônes adaptées aux types d'équipements
    * différenciation visuelle des regroupements selon leur statut et importance
    * différenciation visuelle des équipements selon s'ils sont associés à un regroupement ou non
    * légende lisible et exhaustive

* Reprise à zéro des formulaires (infobulles, champs interactifs, tableaux des données liées, méthode des équipements et regroupements…)
* Automatisation :

    * les associations entre équipements et regroupements se font automatiquement à la création des entités
    * champ ``producteur`` renseigné automatiquement selon le nom de l'organisation associée au compte de l'utilisateur
    * l'importance d'un regroupement est déterminée selon les équipements qui lui sont associés

* Nouveaux champs :

    * Login du compte ayant créé/modifié la donnée
    * Date de création/modification
    * Distance entre un équipement et son regroupement associé
    * Distance entre un regroupement et les itinéraires auxquels il est associé

* Davantage de couches disponibles :

    * autres véloroutes (sur lesquelles il n'y a pas de dynamique de numérisation d'équipements)
    * limites administratives IGN
    * Plan IGN
    * Photographie aérienne IGN

* Possibilité de filtrer les couches ``Equipement`` et ``Regroupement`` selon les valeurs des champs
* Recherche des équipements et regroupements par leur identifiant ou leur nom
* Données équipements et regroupements disponibles à l'export via le requêteur (licence ODbL)
* Mise en place d'un système de restriction géographique (empêche de modifier des données en-dehors de sa collectivité ou de son itinéraire)
* Mise à jour du dictionnaire de données du référentiel national (gabarits, correspondance avec OpenStreetMap…)
* Protection des données personnelles : les logins des créateurs et modificateurs des données n'apparaissent que pour les utilisateurs connectés et sont exclus des exports de données
* Impossibilité d'associer un regroupement à un itinéraire trop lointain
* Optimisation des performances des couches affichées
