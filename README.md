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

Les séances sont organisées en format atelier. Chaque séance comportera une dimension pratique, avec des temps d'application et exercices sur des cas concrets. Le module est organisé en séquences progressives : (1) installation de l’environnement de travail, (2) , (3) réalisation de différents types d'analyse statistique.

Bloc 1 – Mise en place & premiers pas (2 séances)  
*Objectif : permettre à chacun·e de disposer d’un environnement de travail fonctionnel*

- Présentation du cours et des attendus
- Installation des environnements de développement (VS Code ou Google Colab) et prise en main
- Exécution des premières lignes de codes à partir d'un exemple fourni par l'enseignants

Bloc 2 – Initiation à R et  (4 séances)  
*Objectif : acquérir les bases de la programmation et du traitement de données*

- Syntaxe de base en Python
- Introduction à Pandas : chargement de bases, nettoyage, recodage, analyse
- Manipulation de variables et statistiques descriptives
- Préparation des données pour la visualisation

Bloc 3 – Visualisation de données (6 séances)  
*Objectif : maîtriser les grands types de visualisation selon la nature des variables*

- Visualisations univariées : histogrammes, barplots, boxplots
- Visualisations bivariées : scatterplots, courbes, boxplots croisés
- Visualisations cartographiques : initiation à la visualisation spatiale (hexbin maps, cartes choroplèthes)

<!-- TODO: raffiner les types de visualisation qui seront présentées -->

## Présentation des données

## Calendrier et créneaux horaire

Selon le groupe et l'enseignant.

## Modes de validation

Le module propose une évaluation reposant sur la remise de rendus intermédiaires et la production d'un rendu final.

| Évaluation                                                              | Poids | Description                                                                 |
|---------------------------|-----------------|-----------------------------|
| Modifications de titres/sous-titres                                     | 10%   | Capacité à choisir des éléments éditoriaux clairs et pertinents             |
| Identification de deux variables et calcul de statistiques descriptives | 10%   | Rigueur dans le choix des variables et la qualité du traitement             |
| Prototype de visualisation univariée                                    | 10%   | Pertinence du graphique et lisibilité                                       |
| Prototype de visualisation bivariée                                     | 10%   | Pertinence du graphique et lisibilité                                       |
| Figure finale                                                           | 60%   | Une visualisation aboutie, respectant tous les critères de qualité attendus |



### Bibliographie

<!-- TODO : COMPLÉTER LA BIBLIO -->
- <>

## À propos de l’enseignant-e
<!-- TODO :  -->

Grégoire Le Campion est ingénieur d'études au CNRS en traitement et analyse de bases de données au sein de l'UMR Passages.