# Documentation Fonctionnelle : Rapport - analyse DPE Enedis

## 1. Présentation du Projet

Cette application Power BI permet d'analyser la performance énergétique des **maisons individuelles** en France sur une période allant du **1er janvier 2024 au début décembre 2025**.

------------------------------------------------------------------------

## 2. Fonctionnalités et Navigation

L'interface est conçue pour une utilisation fluide grâce à des éléments de contrôle persistants :

-   **Réinitialisation des filtres ajoutés :** Un clic sur le **Logo Enedis** (en haut à gauche) réinitialise l'ensemble des filtres et segments sur la page active pour revenir à la vue par défaut.
-   **Navigation :** L'utilisateur peut passer d'une analyse à l'autre via les **flèches de navigation** situées en bas à droite de l'écran.
-   **Interactivité :** Toutes les visualisations sont croisées ; cliquer sur un segment de graphique filtre automatiquement le reste de la page.

------------------------------------------------------------------------

## 3. Analyse des Pages et Visualisations Clés

### Page 1 : Synthèse des DPE

*L'intérêt de cette page est de fournir une vue "Directoire" pour comprendre l'état global du parc.*

-   **Indicateurs Clés (KPIs) :** Volume des DPEs, la consommation moyenne ( en $kWh/m^2$), le coût moyen annuel et la surface moyenne des logements.
-   **Répartition par Étiquette :** Histogramme permettant d'identifier la classe énergétique dominante (
-   **Évolution Temporelle :** Comparaison des courbes de consommation entre 2024 et 2025 avec hiérarchie des dates (Année \> Trimestre \> Mois \> Jour) pour détecter les tendances saisonnières.
-   **Mix Énergétique :** Un graphique circulaire identifiant les 3 énergies les plus consommées (Gaz, Électricité, Fioul).

### Page 2 : Analyse des DPE

*Cette page est dédiée à l'exploration technique et géographique des données.*

-   **Focus Performance :** Mise en avant du taux de "passoires thermiques" soit les DPE : E F ou G et du taux de pénétration des **EN**ergies **R**enouvelables (ENR).
-   **Répartition par Usage :** Analyse détaillée des consommations secondaires (Éclairage, Refroidissement, Auxiliaire) selon le type d'énergie.
-   **Cartographie :** Une carte chlorophètre de France interactive permettant de visualiser la répartition de la consommation par département.
-   **Top 5 Départements :** Classement des zones géographiques ayant la consommation moyenne la plus élevée.
-   **Nuage de points :** Sur les etiquettes de Gaz à Effet de Serre montrant l'impact environmental du logement en fonction de sa surface et de ses consommations 5 usages. 

### Page 3 : Comparaison Ville la plus chaude vs la plus froide

*Page de "Comparaison" climatique comparant les communes de **Mouthe** (Doubs), ville la plus froide de France et **Villevieille** (Gard) la plus chaude.*
> A savoir, cette feuille possède un filtrage forcé sur les deux codes postaux des deux communes concernées.

-   **Visualisation par Jauge :** Comparaison directe de la consommation moyenne. Elle met en évidence l'impact du climat sur la dépense énergétique (Mouthe consommant environ deux fois plus que Villevieille).
-   **Analyse Comparative :** Comparaison des étiquettes DPE et des coûts par code postal pour évaluer si l'isolation compense la rigueur climatique.
-   **Filtres forcés :** Contrairement aux pages précédentes, celle-ci est verrouillée sur ces deux localités pour garantir une analyse comparative stable.
-   **Score BAN :** Ce score correspond à la précision des données géographiques dans ce jeux de données (100% correspond a un lieu parfaitement rempli).

------------------------------------------------------------------------

## 4. Rôles et Administration

-   **Utilisateurs ciblés :** Analystes de données énergétiques, par département ou rôle admin avec tous les droits
-   **Mise à jour:** Les données couvrent la période 2024-2025. Une mise à jour annuelle est recommandée pour intégrer les nouveaux diagnostics.

