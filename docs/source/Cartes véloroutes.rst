Cartes véloroutes
=================

.. note::
    Page en construction.

Le Réseau vélo et marche anime, avec le soutien du Ministère de la transition écologique et de la cohésion des territoires, `L'Observatoire national des véloroutes <https://www.velo-territoires.org/observatoires/observatoire-national-des-veloroutes-et-voies-vertes/>`_ qui vise à suivre l'évolution des véloroutes et notamment l'avancement de leur réalisation. Toutes les véloroutes sont concernées, du niveau européen au départemental. Les données proviennent des collectivités contributrices, elles sont mises en qualité et en cohérence par le Réseau vélo et marche, puis diffusées sur Velodatamap.

La carte « Véloroutes » a deux utilités principales :

- **visualiser** les véloroutes et interroger les données à une échelle fine (accessible sans compte) ;
- **diffuser** les données via du téléchargement ponctuel (accessible sans compte) ou directement auprès de partenaires sélectionnés (France Vélo Tourisme, etc.)

Un **webinaire** de présentation de cette carte s'est tenu en octobre 2024, dont vous pouvez visionner l'enregistrement `ici <https://www.velo-territoires.org/ressources/videotheque/explorer-et-telecharger-les-donnees-de-lobservatoire-national-des-veloroutes/>`_.

Structure des données
---------------------
La structuration des données sur véloroutes s'inspire largement du `Géostandard des véloroutes et voies vertes <https://www.velo-territoires.org/politiques-cyclables/data-velo-modeles-donnees/geostandard-veloroutes-voies-vertes/>`_ (sans en reprendre toute la complexité), qui décrit notamment trois données nécessaires à la description d'une véloroute, correspondant à trois niveaux de granularité :

- l'**itinéraire** : c'est l'élément structurant du réseau, inscrit dans un schéma de développement de réseau cyclable de niveau européen, national, régional ou départemental ;

- la **portion** cyclable : elle indique pour les véloroutes concernées, les étapes réalisables à la journée telles que conçues par le Comité d'itinéraire, mais aussi les éventuelles variantes et sections provisoires ;

- le **segment** cyclable : élément le plus fin du réseau des véloroutes qui correspond à un tronçon cyclable identifiable par sa géométrie, son avancement ou encore le type de voirie ;

Une quatrième donnée vient compléter la description des véloroutes :

- la **liaison** cyclable : parcours balisé assurant la desserte locale d'un point d'intérêt particulier tel qu'un pôle intermodal, un site touristique ou un service.


Interroger des données
---------------------
Les cartes Véloroutes présentent les 4 données décrites ci-dessus, chacune étant matérialisée par une couche sur la carte, à l'exception de la données segment cyclable. Cette dernière propose en effet 3 représentations différentes et complémentaires (et donc 3 couches sur la carte) pour répondre au mieux aux de différents besoins visualisation des utilisateurs.


Pour savoir comment interroger, filtrer ou télécharger les données, lisez la page des :ref:`Fonctionnalités générales`.

.. note::
    Le requêteur vous donne accès aux trois granularités de données véloroute : itinéraire, portion et segment, ainsi qu'à la donnée liaison. Faites votre choix en cliquant sur le bon onglet :
    
    .. figure:: images/onglets_requeteur_veloroutes.png
       :width: 930
