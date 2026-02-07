# Documentation Technique : Rapport - analyse des DPE

## I. Modèle de Données

### 1. Schéma Général

L’architecture de l’application repose sur un modèle en étoile. Cette structure permet d’optimiser les performances et de faciliter les analyses croisées entre dimensions.

### 2. Tables de Dimensions

-   **D_Date**\
    Dimension temporelle générée dynamiquement afin d’intégrer les notions d’année, de mois, de trimestre et de semestre.

-   **D_Batiment**\
    Table regroupant les caractéristiques techniques des logements, incluant les étiquettes DPE et GES, le type de bâtiment, la zone climatique et le type d’énergie principale de chauffage.

-   **D_Localisation**\
    Table géographique contenant les codes départementaux BAN, les codes INSEE, les codes postaux ainsi que les coordonnées spatiales X et Y.

### 3. Table de Faits

-   **F_DPE**\
    Table centrale regroupant les indicateurs quantitatifs : consommations énergétiques par usage, consommation de chauffage, éclairage, coûts annuels estimés et surface habitable.

## II. Préparation des données (Power Query)

### 1. Sources de Données

Les données sont chargées à partir d'un fichier CSV statique provenant d'un ADEME et Enedis.

### 2. Processus de nettoyage

-   Suppression des lignes vides afin d’assurer la fiabilité des calculs statistiques
-   Typage strict des colonnes pour garantir la cohérence des agrégations
-   Nettoyage et standardisation des noms de colonnes
-   Suppression des colonnes non exploitées pour optimiser la taille du modèle

## III. Logique Métier et Indicateurs

### 1. Harmonisation des types d’énergie

Les différentes sources d’énergie sont regroupées par catégories afin de simplifier l’analyse et d’améliorer la lisibilité des visualisations.

### 2. Indicateur logement éco

Un indicateur métier permet d’identifier la proportion de logements utilisant des énergies renouvelables ou des réseaux de chaleur, facilitant l’analyse de la performance énergétique globale du parc immobilier.

## IV. Sécurité des données (RLS)

### 1. Principe général

Des règles de sécurité au niveau des lignes ont été définies afin de restreindre l’accès aux données selon le profil utilisateur.

### 2. Rôle Configuré

-   **Analyste départemental**\
    Accès limité aux données correspondant à un seul département via un filtrage automatique sur le code département BAN.
-   **Admin**\
    Accès illimité aux données.
    
### 3. Objectif

Garantir la confidentialité des données tout en maintenant une analyse pertinente à l’échelle territoriale.

## V. Analyse des performances

### 1. Diagnostic global

Le rapport présente une bonne réactivité avec un temps de chargement moyen largement inférieur à une seconde (200ms sur filtrage des DPEs).

### 2. Facteurs de performance

-   Utilisation d’un modèle en étoile optimisé
-   Relations simples entre tables de dimensions et table de faits
-   Calculs optimisés limitant la complexité des requêtes

### 3. Visuels

Les cartes et graphiques d’évolution temporelle sont les éléments les plus consommateurs en ressources, mais restent fluides grâce à l’optimisation globale du modèle.


