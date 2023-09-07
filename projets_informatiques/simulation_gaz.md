### Simulation d'un gaz rare
<!--
Pour comprendre les phénomènes physiques à l'échelle moléculaire, on peut avoir recours aux simulations. Dans ce projet, vous allez construire votre propre programme de simulation pour étudier le comportement d'un liquide de sphères de Lennard-Jones, un modèle couramment utilisé pour les atomes non polaires, comme l'argon liquide. La méthode utilisée sera la méthode de Monte-Carlo pour un système où le nombre de particules, le volume et la température de la simulation sont fixés. Vous vérifierez la convergence du système vers un état d'équilibre, ainsi que la précision de votre modèle en comparant quelques points de l'équation d'état obtenus dans les simulations avec des données expérimentales.
-->
#### Démarche proposée

1. Étudier le modèle de sphères de Lennard-Jones et son utilisation pour modéliser les interactions entre particules non polaires.

2. Définir les paramètres de la simulation (nombre de particules, volume du conteneur, température, ...) et générer les positions initiales des particules dans le conteneur.
3. Tenir compte de conditions périodiques
4. Implémenter le déplacement des atomes dans la boîte en utilisant la méthode de Monte Carlo et l'algorithme de Metropolis
5. Surveiller les propriétés du système pour observer la convergence vers un état d'équilibre.
7. Calculer l'équation d'état du système ($\beta P$ en fonction de $\rho$)) à partir des propriétés mesurées et les comparer à des valeurs expérimentales.


##### Liens utiles

- [Chapitre de livre](https://dasher.wustl.edu/chem430/readings/frenkel-montecarlo.pdf) *Molecular Simulations* de Frenkel et Smit : pseudocodes pour implémenter un algorithme de simulation moléculaire

[Haut de la page](#simulation-dun-gaz-rare)

[Retour page](/projets_informatiques/sujets_AH.md#projets-informatiques-chimie-paris-proposé-par-arthur-hardiagon)