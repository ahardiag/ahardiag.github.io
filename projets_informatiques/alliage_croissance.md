---
layout: default
title: Projets Informatiques
description: Alliage et phénomène de croissance
---

## Alliage et phénomène de croissance

Les alliages métalliques sont des matériaux composites constitués de deux ou plusieurs éléments métalliques qui présentent des propriétés mécaniques et physiques améliorées par rapport aux métaux purs. La microstructure de ces alliages, influencée par la répartition des différents atomes, joue un rôle crucial dans leurs propriétés macroscopiques, telles que la dureté, la résistance à la corrosion, et la conductivité électrique. Pour comprendre et prédire la formation de cette microstructure, les modèles de physique statistique, comme le modèle d'Ising, sont souvent utilisés. Le projet consistera à identifier dans le modèle d’Ising avec dynamique conservée de Kawasaki deux propriétés particulières que l’on retrouve dans les alliages :

- La température de Curie : température au-delà de laquelle les deux éléments sont complètement mélange
- Le phénomène de « slow cooling » qui permet d’obtenir des phases stable 

### Démarche proposée

1) Lire la doc sur le modèle d'Ising 2D
2) Écrire un premier code du modèle d'Ising avec un dynamique conservée (dynamique de Metropolis) et vérifier qu'il fonctionne en utilisant les données théoriques sur ce modèle
3) Définir un alliage 2D à 50%/50% de deux métaux A et B et utiliser la dynamique de Kawasaki pour étudier l'évolution du système
4) Déterminer la température de Curie du système
5) Étudier la croissance des domaines
6) Proposer un protocole pour obtenir une phase stable donnée à une température T<Tc

### Modèle d'Ising

Pour modéliser un alliage constitué de deux types d'atome A et B, on peut utiliser le modèle d'Ising où l'interaction entre les atomes est assimilé à des interactions magnétiques entre spins.

$$
E = - \sum_{i \in \partial j} J_{ij} S_{i} S_{j} - B \sum_{i=1}^{N} S_{i}
$$

où $J_{ij}$ est la constante de couplage entre deux spins voisins et B le champ magnétique moyen appliqué à l'ensemble du système et $$\{ S_i \}_{i=0..N}$$ l'ensemble des N spins ou variables à deux états : $S_i=1$ ou $-1$.
Les atomes étant identiques, on a $J_{ij} = J$, on pourra prendre dans un premier temps $B = 0$ (pas de perturbation extérieure du système) et J>0 (interaction type ferromagnétique).

### Algorithme de Metropolis

Pour faire évoluer le système vers un état d'équilibre qui échantillonne correctement les configurations selon la loi de probabilité de Boltzmann : $$ P(\{S_i\}_{i=0..N}) \propto exp(-\frac{E(S_1,S_2,.., S_N)}{k_BT}) $$, on peut utiliser l'algorithme de Metropolis suivant :

1. **Initialiser** la grille de spins.
2. **Définir** les paramètres : J, B ,T, $ \beta = \frac{1}{k_B T} $.
3. **Pour chaque itération** :
   - Sélectionner un spin aléatoire $S_i$.
   - Calculer l'énergie $\Delta E$ du changement de spin :
     $$
     \Delta E = 2 \cdot S_i \cdot (J \cdot \text{somme voisins} + B)
      $$
   - Si $$\Delta E < 0$$ ou avec probabilité $$ p = \exp(-\beta \cdot \Delta E) $$, inverser $S_i$.
4. **Répéter** jusqu'à $$N_{\text{iter}}$$ itérations.

Metropolis fait fartie des algorihmes dit de dynamique non-conservative, cela signinfie que la magnétisation totale $M = \sum_{i=1..N} S_i$ n'est pas constante.

Dans le cas d'un réseau 2D à géométrie carrée, le nombre de spins totale est donnée par $N = L²$, avec $L$ la taille du système.

### Dynamique de Kawasaki

Dans le cas de Kawasaki, la dynamique est conservative, c'est-à-dire que la magnétisation totale est constante, cette dynamique peut donc être utilisé pour modéliser l'évolution d'un mélange de deux espèces dont leur quantité de matière reste constante au cours du temps. Dans la dynamique de Kawasaki, on échange deux spins voisins et on utilise un critère sur la variation d'énergie similaire à l'algorithme précédent, le pseudo-code de l'algorithme est le suivant :

1. **Initialiser** la grille de spins.
2. **Définir** les paramètres : J, B, T, $$\beta = \frac{1}{k_B T} $$.
3. **Pour chaque itération** :
   - Choisir deux spins aléatoires $S_i$ et $S_j$.
   - Calculer l'énergie avant $$(E_{\text{initial}})$$ et après $$(E_{\text{final}})$$ la permutation des spins.
   - Calculer la différence d'énergie $\Delta E$
   - Accepter la permutation avec probabilité $$ \min(1, \exp(-\beta \cdot \Delta E)) $$.
4. **Répéter** jusqu'à ce que toutes les itérations soient complètes.

## Conditions aux bords
Le nombre d'atomes possibles dans une simulations est contraint par le temps d'execution des simulations. On peut cependant s'approcher d'un milieu fini

### Taille des domaines

Pour déterminer la vitesse de croissance des domaines (zones de même magnétisation), plusieurs approches sont possibles :
- à partir de **l'énergie du système** :
$$
$$
- à partir du **nombre de paires de spins opposés** (ou surface de contact) $N_c$:
$$
L_c \propto \frac{L^2}{N_{c}/2}
$$
- à partir de la **fonction de corrélation de paires** $$g(r) = \langle S_i S_j \rangle $$

### Références

- Cours de classe préparatoire sur le modèle d'Ising 2D : [Modèle d'Ising 2D](https://femto-physique.fr/simulations/ising2D.php#menu)
- Amar, J. G.; Sullivan, F. E.; Mountain, R. D. Monte Carlo Study of Growth in the Two-Dimensional Spin-Exchange Kinetic Ising Model. Phys. Rev. B 1988, 37 (1), 196–208. https://doi.org/10.1103/PhysRevB.37.196.

[Retour page](sujets_AH_24-25.md)