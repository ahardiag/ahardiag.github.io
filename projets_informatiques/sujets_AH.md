## Projets Informatiques

Ces projets sont destinés aux étudiants de ChimieParisTech A2 au premier semestre 2023/2024.

### Allocation de rôles dans un réseau

Imaginez que vous soyez responsable de la gestion d'une équipe formée de membres ayant des compétences variées et des préférences spécifiques en matière de tâches. Chaque membre de l'équipe dispose d'une liste de rôles qu'il souhaite occuper et d'autres qu'il préférerait éviter (comme par exemple le rôle de coordinateur ou d'expert technique). Pour chaque tâche, il est nécessaire qu'au moins un membre de l'équipe se voie assigner un rôle préféré et un rôle non préféré. Cette contrainte assure une distribution équilibrée des tâches au sein de l'équipe. Dans un contexte où les individus travaillent sur plusieurs tâches en équipes formées au hasard, la répartition des rôles devient un problème NP-complet, connu sous le nom de NAE-SAT (Not-All-Equal-Satisfiability). La résolution de ce problème pour toutes les instances possibles à l'aide d'un algorithme en temps polynomial n'est pas possible. Vous proposerez un algorithme permettant de trouver une solution du problème NAE-3-SAT pour des instances générées aléatoirement.

[Pour aller plus loin](./allocation_roles_reseau.md)

### Surface d'une molécule

L'examen approfondi de la surface des molécules biologiques, en particulier des protéines, revêt une importance capitale pour élucider leur structure, ce processus ayant des répercussions significatives sur des aspects essentiels tels que leurs fonctions, leur stabilité et leur réactivité. Vous écrirez un programme informatique permettant de calculer la surface moléculaire d'une protéine ou, dans un premier temps d'une petite molécule, à partir de sa structure PDB. Vous pourrez utiliser une méthode de votre choix, analytique ou discrète.

[Pour aller plus loin](./surface_molecule.md)

### Simulation d'un gaz rare

Pour comprendre les phénomènes physiques à l'échelle moléculaire, on peut avoir recours aux simulations. Dans ce projet, vous allez construire votre propre programme de simulation pour étudier le comportement d'un liquide de sphères de Lennard-Jones, un modèle couramment utilisé pour les atomes non polaires, comme l'argon liquide. La méthode utilisée sera la méthode de Monte-Carlo pour un système où le nombre de particules, le volume et la température de la simulation sont fixés. Vous vérifierez la convergence du système vers un état d'équilibre, ainsi que la précision de votre modèle en comparant quelques points de l'équation d'état obtenus dans les simulations avec des données expérimentales.

[Pour aller plus loin](./simulation_gaz.md)

[Retour page](../README.md)