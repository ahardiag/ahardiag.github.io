---
layout: default
title: Projets Informatiques
description: Ressources
---

## Projets Informatiques

Projets proposés aux étudiants de Chimie ParisTech 2ème année au  premier semestre 2023/2024.

### Surface d'une molécule

L'examen approfondi de la surface des molécules biologiques, en particulier des protéines, revêt une importance capitale pour élucider leur structure, ce processus ayant des répercussions significatives sur des aspects essentiels tels que leurs fonctions, leur stabilité et leur réactivité. Vous écrirez un programme informatique permettant de calculer la surface moléculaire d'une protéine ou, dans un premier temps d'une petite molécule, à partir de sa structure PDB. Vous pourrez utiliser une méthode de votre choix, analytique ou discrète.

[Pour aller plus loin](./surface_molecule.md)

### Simulation d'un gaz par un algorithme de Monte-Carlo

Pour comprendre les phénomènes physiques à l'échelle moléculaire, on peut avoir recours aux simulations. Dans ce projet, vous allez construire votre propre programme de simulation pour étudier le comportement d'un liquide de sphères de Lennard-Jones, un modèle couramment utilisé pour les atomes non polaires, comme l'argon liquide. La méthode utilisée sera la méthode de Monte-Carlo pour un système où le nombre de particules, le volume et la température de la simulation sont fixés. Vous vérifierez la convergence du système vers un état d'équilibre, ainsi que la précision de votre modèle en comparant quelques points de l'équation d'état obtenus dans les simulations avec des données expérimentales.

### Sujet : Réseau sous contraintes

Imaginez que vous êtes à la tête d'une entreprise de livraison qui livre des matières premières pour des chantiers. Chaque jour, vous avez N livreurs et N chantiers. Pour optimiser les coûts de livraisons, vous mettez en relation chaque chantier avec k livreurs tirés au hasard. Quel type de marchandise chaque livreur doit prendre dans sa journée pour éviter que tous les livreurs d'un même chantier livre la même marchandise ? En désignant les marchandises par des couleurs, ce problème revient à résoudre le problème de coloriage sur hypergraphes. C'est un problème NP-complet, lorsque le nombre M/N est grand, il devient très dur à résoudre. Vous concevrez un programme en C qui génère des instances aléatoires de ce problème et trouve une solution à l'aide de la méthode de recuit simulé. Vous évaluerez dans un second temps la limite M/N au delà de laquelle votre algorithme échoue.

Kose, A.; Sonmez, B. A.; Balaban, M. Simulated Annealing Algorithm for Graph Coloring. arXiv December 3, 2017. http://arxiv.org/abs/1712.00709 (accessed 2023-10-31).

[Pour aller plus loin](./allocation_roles_reseau.md)

### Sujet : Equilibration de charges

Dans une simulation moléculaire classique, les charges atomiques sont des paramètres régissant la force des interactions électrostatiques. Pour étudier une grande diversité de molécules, dont des molécules récemment découvertes et non étudiées, on a besoin d'automatiser la paramétrisation des charges. Parmi différentes méthodes existantes, la méthode d'équilibration de charges QEq est intéressante car elle détermine les charges partielles sur une molécule quelconque à partir de la seule géométrie de la molécule et des propriétés atomiques, comme les énergies de ionisation, l'affinité atomique et les rayons atomiques et ne nécessite pas de calcul ab-initio coûteux. Le projet consistera à implémenter en C cette méthode de minimisation, et tester sa précision sur des molécules simples comme des acides aminés ou peptides.

(1) Rappe, A. K.; Goddard, W. A. I. Charge Equilibration for Molecular Dynamics Simulations. J. Phys. Chem. 1991, 95 (8), 3358–3363. https://doi.org/10.1021/j100161a070.
(2) Wilmer, C. E.; Kim, K. C.; Snurr, R. Q. An Extended Charge Equilibration Method. J. Phys. Chem. Lett. 2012, 3 (17), 2506–2511. https://doi.org/10.1021/jz3008485.


### Sujet : Simulation Boltzmann sur réseau

Les systèmes chimiques industriels impliquent souvent des fluides complexes, tels que les suspensions colloïdales ou les émulsions. Ces fluides sont composés de petites particules en suspension dans un liquide, et leur comportement est régi par des interactions complexes. Les simulations mésoscopiques comme la méthode Boltzmann sur réseau peuvent être utilisées pour modéliser la dynamique de ces systèmes sur des échelles de temps et de longueur intermédiaires. Votre projet consistera à écrire un programme en langage C qui permet de simuler un champ de vitesse dans un fluide homogène à l'aide de la méthode de Boltzmann sur réseau. Des systèmes simples de mécanique des fluides pourront être utilisés pour valider la méthode, en 2D puis en 3D. L'objectif suivant, si le temps le permet sera de modéliser l'écoulement des fluides autour d'obstacles.

(1) [La méthode de Boltzmann sur réseau](https://bupdoc.udppc.asso.fr/consultation/article-bup.php?ID_fiche=22451) : utilisation en mécanique des fluides, Thierry PRÉ, François HERNANDEZ


### Sujet : Simulation d'un liquide par dynamique moléculaire

Pour comprendre les phénomènes physiques à l'échelle moléculaire, on peut avoir recours aux simulations. Dans ce projet, vous allez construire votre propre programme de simulation pour étudier le comportement d'un liquide de sphères de Lennard-Jones, un modèle couramment utilisé pour les atomes non polaires, comme l'argon liquide. La méthode utilisée sera la méthode de Dynamique Moléculaire pour un système où le nombre de particules, le volume et l'énergie du système sont fixés. Vous vérifierez la convergence du système vers un état d'équilibre, ainsi que la précision de votre modèle en comparant quelques points de l'équation d'état obtenus dans les simulations avec des données expérimentales. Si le temps vous le permez, vous modifierez votre programme pour fixer la température au lieu de l'énergie du système.

(1) Verlet, L. Computer “Experiments” on Classical Fluids. I. Thermodynamical Properties of Lennard-Jones Molecules. Phys. Rev. 1967, 159 (1), 98–103. https://doi.org/10.1103/PhysRev.159.98.


[Pour aller plus loin](./simulation_gaz.md)

[Retour page](../README.md)