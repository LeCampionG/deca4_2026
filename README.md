# Description de l’atelier

## Présentation

<!-- TODO: -->
Cet atelier propose une initiation à la statistique spatiale avec R, pour apprendre à analyser des données en tenant compte des effets liés à la dimension spatiale et géographique des données. Nous réaliserons un tour d’horizon des différents modèles et insisterons davantage sur ceux permettant d’étudier l’hétérogénéité spatiale des phénomènes étudiés ou comment des effets peuvent varier en fonction des lieux !
Cette réflexion sera également l’occasion d’une introduction à la cartographie avec R (package mapsf) mais également avec le logiciel « clique-bouton » en ligne Magrit (<https://magrit.cnrs.fr/>) pour représenter nos résultats.

## Contenu et validation :

Aucun prérequis technique n’est nécessaire (ni en statistiques, ni en R, les ). L’atelier est pensé pour un public qui souhaite mieux comprendre les enjeux géographiques et du spatial dans l’analyse de données. Pour ce faire nous utiliserons un exemple concret visant à expliquer le prix de l’immobilier par EPCI en France Hexagonale. La validation passera par la remise d’un dossier reprenant le processus d’analyse de statistique spatiale tel qu’il aura été présenté, analyse qui se basera sur des données qui auront été fournies.

## Exemple d’illustrations qui pourront être réalisées

![LISA](images/example1.png)

![collection](images/example2.png)

![nb](images/example3.png)


## Objectifs et organisation de l’atelier

### A la fin du semestre, vous saurez

-	Comprendre pourquoi et comment intégrer l’espace dans une analyse statistique
-	Utiliser R et Magrit pour produire des cartes et des statistiques spatiales
-	Mobiliser les outils de base de la statistique spatiale (GWR, LISA)
-	Interpréter et représenter les résultats d’une analyse de statistique spatiale sur un cas réel


### Descriptif général
<!-- PRÉCISER BASE -->
Lorsque l’on étudie des phénomènes complexes en sciences humaine et social, il est très fréquent que les effets, les explications, etc. de ces phénomènes varient en fonction du lieu. La grande question c’est pourquoi des effets des tendances sociales ou économiques observées à Paris ne sont pas les mêmes à Marseille, ou inversement ? Ce type de questions suppose en réalité de tenir compte de l’espace dans nos analyses. En tant que « pratiquant » des SHS on le conçoit intuitivement. En revanche, la statistique elle, a beaucoup plus de mal à l’appréhender. En effet, dès qu’il est question de spatial la statistique « classique » risque fort d’être inopérante.

En effet, les données spatiales posent un défi important aux modèles en statistique « classique ». Selon la première loi de la géographie formulée par Tobler – « Tout interagit avec tout, mais deux objets proches ont plus de chance de le faire que deux objets éloignés » – les données géographiques sont naturellement auto-corrélées, ce qui va à l’encontre du principe d’indépendance requis en statistique classique.
La statistique spatiale présente comme premier intérêt majeur de permettre de dépasser certaines limites de la statistique classique.
En effet, cette dépendance spatiale rend difficile l’application des modèles traditionnels, comme la régression linéaire. La statistique spatiale constitue donc une alternative à la statistique classique et permet d’intégrer la dimension spatiale à nos modèles.

Au-delà de la contrainte technique, la statistique spatiale présente un autre intérêt majeur : tenir compte du spatial nous permet plus largement de comprendre d’un point de vue statistique comment les comportements ou les dynamiques sociales peuvent varier selon les territoires ou nos voisins.
Il devient ainsi possible d’étudier l’effet des voisins sur nos individus (dépendance spatiale) ou encore d’étudier la fluctuation des effets en fonction des lieux (hétérogénéité spatiale) deux phénomènes particulièrement intéressant dans l’analyse des phénomènes en SHS.

À partir d’un exemple concret (l’analyse des prix de l’immobilier en France hexagonale), nous découvrirons des méthodes qui permettent :
-	d’identifier si des zones géographiques présentent des dynamiques similaires ou différentes (analyse LISA),
-	d’observer si les relations entre variables changent selon les lieux (régression géographiquement pondérée ou GWR),
-	et de représenter ces résultats sur des cartes claires et parlantes.

Nous utiliserons pour cela le langage R ainsi que des outils simples comme Magrit, un logiciel de cartographie en ligne.


### Format du cours et programme prévisionnel

Les séances sont organisées en format atelier. Chaque séance comportera une dimension pratique, avec des temps d'application et exercices sur des cas concrets. Le module est organisé en séquences progressives : (1) installation de l’environnement de travail, (2) COmprendre l'intért de la statistique spatiale, (3) réalisation de différents types d'analyse statistique spatiale , (4) Initiation à la carto avec Magrit et (5) une ouverture vers les autres méthodes de la statistique spatiale

Bloc 1 – Mise en place & premiers pas (2 séances)  
*Objectif : permettre à chacun·e de disposer d’un environnement de travail fonctionnel*

- Présentation du cours et des attendus
- Installation des environnements de développement et prise en main
- Exécution des premières lignes de codes à partir d'un exemple fourni par l'enseignant

Bloc 2 – Pourquoi la statistique spatiale  (2 séances)  
*Objectif : comprendre l'intéret d'utiliser la statistique spatiale*

- Comprendre la différence entre homogénité et hétérogénéité spatiale
- Présenter un panorama des différentes méthodes de la statistique spatiale
- Comprendre pourquoi la statistique classique ne gère pas correctement la donnée spatiale
- Préparation des données pour la visualisation

Bloc 3 – Visualisation de données (5 séances)  
*Objectif : réaliser et maîtriser les principales analyses du champs de l'hétérogénéité spatiale*

- Réaliser sur R une analyse des LISA
- Réaliser 

Bloc 4 - Initiation à Magrit (2 séances)
*Objectif : s'initier à la réalisation de cartes à laide du logiciel clic-boutons Magrit*

- Se familiariser avec l'interface
- Réaliser ses premières cartes

Bloc 5 - Ouverture vers les autres méthodes de la statistique spatiale (1 séances)
*Objectif : présenter également les autres méthodes de la staistique spatiale*

- Présenter les différentes régressions spatiales
- Présenter la MGWR
- Présenter les méthodes de régionnalisation


<!-- TODO: raffiner les types de visualisation qui seront présentées -->

## Présentation des données utilisé dans le cadre de l'atelier


| Nom | Résumé | Source | Notes |
|--- |--- |--- |--- |
| data_marseille.csv | Données de pauvreté par IRIS pour Marseille (cf. détail des variables ci-dessous) | INSEE https://www.insee.fr/fr/statistiques/6049648 | Les variables explicatives ont été centrées-réduites |
| donnees_standr.csv  | Prix médian de l'immobilier par EPCI en France métropolitaine (cf. détail des variables ci-dessous) | base Notaires de France https://www.immobilier.notaires.fr/fr/prix-immobilier | Les variables explicatives ont été centrées-réduites |
| EPCI.shp  | EPCI France métropolitaine + Corse édition 2021 | IGN ADMIN-EXPRESS-COG édition 2021 par territoire https://geoservices.ign.fr/adminexpress | Les données de l'IGN ont été simplifiées avec [mapshaper]([https://mapshaper.org/) pour en réduire le poids, en utilisant l'algorithme *Visvalingam/weighted area* avec une valeur de 1 |
| IRIS13_GE.shp  | Iris recalés sur les données BD TOPO® (précision 1 m) | IGN IRIS…GE® https://geoservices.ign.fr/irisge |  |
| REGION.shp  | Nouvelles régions France métroplitaine + Corse édition 2021 | IGN ADMIN-EXPRESS-COG édition 2021 par territoire https://geoservices.ign.fr/adminexpress  | Les données de l'IGN ont été simplifiées avec [mapshaper]([https://mapshaper.org/) pour en réduire le poids, en utilisant l'algorithme *Visvalingam/weighted area* avec une valeur de 1 |

Le fichier **data_marseille.csv** est le fichier qui sera proposé aux étudiants pour s'approprier le code et les méthodes présentéess. Ce fichier a été constitué à partir de données de l'INSEE. Il contient les variables suivantes (attention, toutes les variables hormis le taux de bas revenu ont été centrées-réduites) :

- id_IRIS : code IRIS
- label_iris : nom de l'IRIS
- code_insee : code INSEE de la commune
- label_com : nom de la commune
- tx_bas_revenu : taux de bas revenus déclarés au seuil de 60% (%) (variable DEC_TP6019 du fichier [BASE_TD_FILO_DEC_IRIS_2019.csv](https://www.insee.fr/fr/statistiques/6049648))
- PartPop_fr : 
- hlm_res_princ : part /personne de résidences principales HLM loué vide en 2017 (%) (variable P17_RP_LOCHLMV du fichier [base-ic-logement-2017](https://www.insee.fr/fr/statistiques/4799305))
- unevoiture : part de ménages disposant au moins d'une voiture en 2017 (%) (variable P17_RP_VOIT1P du fichier [base-ic-logement-2017](https://www.insee.fr/fr/statistiques/4799305))
- res120plus : part de résidences principales de 120 m2 ou plus en 2017 (%) (variable P17_RP_120M2P du fichier [base-ic-logement-2017](https://www.insee.fr/fr/statistiques/4799305))
- masc_cadre : part d'hommes de 15 ans ou plus cadres et professions intellectuelles supérieures (%) (variable C17_H15P_CS3 du fichier [base-ic-evol-struct-pop-2017](https://www.insee.fr/fr/statistiques/4799309?sommaire=4658626))
- fem_noncadre : part de femmes de 15 ans ou plus autres sans activité professionnelle (variable C17_F15P_CS8 du fichier [base-ic-evol-struct-pop-2017](https://www.insee.fr/fr/statistiques/4799309?sommaire=4658626))

L'unité spatiale des données est l'IRIS.Cette unité spatiale a été créee par l'INSEE afin de préparer la diffusion du recensement de la population de 1999, l'INSEE avait développé un découpage du territoire en mailles de taille homogène appelées IRIS2000. Un sigle qui signifiait « Ilots Regroupés pour l'Information Statistique » et qui faisait référence à la taille visée de 2 000 habitants par maille élémentaire.
Depuis, l'IRIS (appellation qui se substitue désormais à IRIS2000) constitue la brique de base en matière de diffusion de données infra-communales. Il doit respecter des critères géographiques et démographiques et avoir des contours identifiables sans ambigüité et stables dans le temps.
Les communes d'au moins 10 000 habitants et une forte proportion des communes de 5 000 à 10 000 habitants sont découpées en IRIS. Ce découpage constitue une partition de leur territoire. La France compte environ 16 100 IRIS dont 650 dans les DOM.
Par extension, afin de couvrir l'ensemble du territoire, on assimile à un IRIS chacune des communes non découpées en IRIS.

Les données utilisés en présentation et en exemple ont été constitué par Frédéric Audard et Alice Ferrari à partir de la base Notaires de France. Il contient les variables suivantes (attention, toutes les variables hormis le prix médian ont été centrées-réduites) :

SIREN : code SIREN de l'EPCI
prix_med : pris médian par EPCI à la vente
perc_log_vac : % logements vacants
perc_maison : % maisons
perc_tiny_log : % petits logements
dens_pop : densité de population
med_niveau_vis : médiane du niveau de vie
part_log_suroccup : % logements suroccupés
part_agri_nb_emploi : % agriculteurs
part_cadre_profintellec_nbemploi : % cadres et professions intellectuelles

Ces données sont à l'échelle de l'EPCI (établissements publics de coopération intercommunale). Les EPCI sont des structures administratives permettant à plusieurs communes d’exercer des compétences en commun.
Ils sont soumis à des règles communes, homogènes et comparables à celles de collectivités locales. Les communautés urbaines, communautés d'agglomération, communautés de communes, syndicats d'agglomération nouvelle, syndicats de communes et les syndicats mixtes sont des EPCI.
(source INSEE)


## Calendrier et créneaux horaire (prévisionnel)

12 séances de 1h30 en salle A 126 :
- jeu. 08/01/2026 09h45
- jeu. 15/01/2026 09h45
- jeu. 22/01/2026 09h45
- jeu. 29/01/2026 09h45
- jeu. 05/02/2026 09h45
- jeu. 12/02/2026 09h45
- jeu. 26/02/2026 09h45
- jeu. 05/03/2026 09h45
- jeu. 12/03/2026 09h45
- jeu. 19/03/2026 09h45
- jeu. 26/03/2026 09h45
- jeu. 02/04/2026 09h45

## Modes de validation

Le module propose une évaluation reposant sur la remise de rendus intermédiaires et la production d'un rendu final.

| Évaluation                                                              | Poids | Description                                        |
|---------------------------|-----------------|-----------------------------|
| Code efficient                                     | 3pts   | Un code qui se déroule sans erreur |
| Analyses des statistiques | 10pts   | Analyse cohérentes de toutes les sorties stat des méthodes présentées             |
| Figures                                    | 3pts   | Production des visuels pertinents avec l'analyse de données |
| Out of the box                                     | 4pts   | Proposition d'analyse plus fine que la simple sortie stat réalisé ou usages d'autres méthodes de la stat spatiale                                       |



### Bibliographie

<!-- TODO : COMPLÉTER LA BIBLIO -->
- <>

## À propos de l’enseignant-e
<!-- TODO :  -->

Grégoire Le Campion est ingénieur d'études au CNRS en traitement et analyse de bases de données au sein de l'UMR Passages.