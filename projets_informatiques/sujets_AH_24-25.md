---
layout: default
title: Projets Informatiques
description: Ressources
---

## Projets Informatiques

Projets proposés aux étudiants de Chimie ParisTech 2ème année au  premier semestre 2024/2025.

### Simulation d'un gaz par un algorithme de Monte-Carlo

Pour comprendre les phénomènes physiques à l'échelle moléculaire, on peut avoir recours aux simulations. Dans ce projet, vous allez construire votre propre programme de simulation pour étudier le comportement d'un liquide de sphères de Lennard-Jones, un modèle couramment utilisé pour les atomes non polaires, comme l'argon liquide. La méthode utilisée sera la méthode de Monte-Carlo pour un système où le nombre de particules, le volume et la température de la simulation sont fixés. Vous vérifierez la convergence du système vers un état d'équilibre, ainsi que la précision de votre modèle en comparant quelques points de l'équation d'état obtenus dans les simulations avec des données expérimentales.

[Pour aller plus loin](./simulation_gaz.md)

### Réseau sous contraintes

Imaginez que vous êtes à la tête d'une entreprise de livraison qui livre des matières premières pour des chantiers. La répartition des livreurs est aléatoire et on ne considèrera pas les facteurs temporels ou la distance des livreurs aux chantiers. Le problème se formule ainsi : Quel type de marchandise doit être assignée à chaque livreur pour éviter qu'un chantier ne manque de matière première ? En désignant les marchandises par des couleurs, ce problème revient à résoudre le problème de coloriage sur hypergraphes. Pour simplifier, on traitera le problème où k=3 (nombre de livreurs par chantiers) et deux couleurs seulement, ce problème est aussi appelé NAE-3-SAT (pour Not-All-Equal 3-satisfiability en anglais). Le but est de trouver au moins une solution à ce problème, quelque soit le tirage aléatoire de la répartition des livreurs, et de déterminer la plage des paramètres pour laquelle l'algorithme fonctionne.

[Pour aller plus loin](./allocation_roles_reseau.md)

### Alliages et croissance de phases

Les alliages métalliques sont des matériaux composites constitués de deux ou plusieurs éléments métalliques qui présentent des propriétés mécaniques et physiques améliorées par rapport aux métaux purs. La microstructure de ces alliages, influencée par la répartition des différents atomes, joue un rôle crucial dans leurs propriétés macroscopiques, telles que la dureté, la résistance à la corrosion, et la conductivité électrique. Pour comprendre et prédire la formation de cette microstructure, les modèles de physique statistique, comme le modèle d'Ising, sont souvent utilisés. Le projet consistera à identifier dans le modèle d’Ising avec dynamique conservée de Kawasaki deux propriétés particulières que l’on retrouve dans les alliages :

- La température de Curie : température au-delà de laquelle les deux éléments sont complètement mélange
- Le phénomène de « slow cooling » qui permet d’obtenir des phases stable 

[Pour aller plus loin](./alliage_croissance.md)


[Retour page](../README.md)