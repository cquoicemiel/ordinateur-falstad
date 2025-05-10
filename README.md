# Construction d’un ordinateur en logique discrète – Projet Falstad

Ce projet a pour objectif la construction progressive d’un ordinateur simple à l’aide du simulateur de circuits logiques **Falstad**. Il s'agit d'un exercice de conception pédagogique visant à comprendre et à expérimenter les bases de l'architecture des ordinateurs à partir de composants logiques élémentaires (portes, bascules, multiplexeurs...).

L'approche est divisée en étapes claires, allant de la simple addition jusqu’à l'exécution de programmes binaires en mémoire. Chaque composant est construit, testé, puis intégré au reste du système.

## Prérequis

- [Simulateur de circuits Falstad](https://www.falstad.com/circuit/)
- Connaissances de base en logique combinatoire et séquentielle

## Étapes du projet

### Étape 1 : Additionneur 8 bits
Je commence par construire un additionneur 8 bits à l'aide d'additionneurs 1 bit reliés entre eux. Cela permet de manipuler les opérations binaires élémentaires.

### Étape 2 : ALU (Arithmetic Logic Unit)
Je construis ensuite une ALU capable de faire des opérations comme l'addition, la soustraction, ET, OU, inversion, et l'égalité à zéro. Ces fonctions sont sélectionnées via des bits de commande.

### Étape 3 : Registres
Je conçois des registres 8 bits qui peuvent stocker une valeur via une horloge (signal de montée). Chaque registre dispose d'une entrée "load" pour choisir s’il faut capturer la valeur ou non.

### Étape 4 : Bus
Je mets en place un bus commun, permettant à différents composants de communiquer. J'utilise des tri-state buffers pour contrôler qui peut écrire sur le bus.

### Étape 5 : Mémoire RAM
Je construis une mémoire RAM simple avec des adresses et des cellules mémoire capables de lire et écrire selon des signaux de contrôle.

### Étape 6 : Compteur de programme (PC)
J’intègre un compteur de programme capable d'incrémenter automatiquement à chaque cycle, ou de charger une nouvelle adresse en cas de saut.

### Étape 7 : Décodeur d'instructions
Je développe un décodeur d'instruction 8 bits qui interprète les instructions codées en binaire, et active les bons signaux pour les registres, l’ALU, la RAM et le PC.

### Étape 8 : Unité de contrôle
Je mets en place une unité de contrôle séquencée qui orchestre chaque cycle d’horloge (fetch, decode, execute).

### Étape 9 : Assembleur + programme
J’écris un petit programme en assembleur pour tester mon ordinateur (par exemple : addition de deux nombres, boucle, condition). Ce programme est codé en binaire et inséré dans la mémoire ROM ou RAM au démarrage.

## Objectif final

Le but est de simuler un ordinateur capable de lire un programme depuis sa mémoire, d'exécuter des instructions simples, et de manipuler des registres et données à travers une architecture cohérente. Cela permet de comprendre en profondeur le fonctionnement d’un CPU et le cheminement des données à bas niveau.
