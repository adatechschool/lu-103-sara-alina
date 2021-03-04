Structures de données – Partie 1 (faite sur Notion)

quand on a une idée des opérations dont on a besoin pour un algorithme, on peut choisir la structure de données la plus adaptée (celle pour laquelle ces opérations sont les moins coûteuses).

Structures de données différentes = opérations différentes 

# Table de hachage (*hash table*) et ses différentes implémentation

- **Quel est son rôle ?Quel est son intérêt ?**

Une table de hachage est une structure de données qui **permet une association clé–valeur**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c09cc0f3-d96b-450f-a3d8-86147eb09531/Capture_decran_2021-03-01_a_15.46.31.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c09cc0f3-d96b-450f-a3d8-86147eb09531/Capture_decran_2021-03-01_a_15.46.31.png)

(les clés sont uniques - les valeurs non) Dans cet exemple : couleurs préférées des gens

—> **Les tables de hachage permettent de retrouver instantanément un élément précis !** 

Si dans les tableaux, pour accéder aux données il fallait savoir le nombre de l'indice, ceci n'est pas nécessaire pour les tables de hachage !

- **Fonction de hachage H(x)** :
    - est une fonction qui associe une clé à une valeur entière d'un interval précis (exemple: pommes —> 1.50 euros)
    - Cette fonction lie aussi l'association valeur-clé à un index précis

**TABLE DE HACHAGE**

= structure de données qui utilisent des FONCTION DE HACHAGE pour trouver où se trouvent stockés les éléments (dans la mémoire)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a0b1c3a7-1598-41df-9f1b-8d796d916f7b/Capture_decran_2021-03-01_a_16.12.20.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a0b1c3a7-1598-41df-9f1b-8d796d916f7b/Capture_decran_2021-03-01_a_16.12.20.png)

- TABLE DE HACHAGE : rapide comme les ARRAYS pour la recherche des éléments, rapide comme les LISTES pour ajouter/éliminer les éléments !!
- **A-t-elle des désavantages ?**
    - Si la fonction de hachage est mauvaise —> bcp de collisions (= plein de couples valeurs-clés stockées au même endroit)
- **Y a-t-il plusieurs façons de s'en servir ?**

- **Quelles sont les étapes importantes pour la mettre en place ?**

    **Implementation simple sur Python :**

    —> dictionnaires (= tables de hacahges)  **dict()**

    **IMPLEMENTATION d'une TABLE DE HACHAGE**

    En C, Les opérations que l'on peut réaliser avec cette table de hachage sont :

    - créer la table (et l'initialiser) ;
    - ajouter une paire clé/valeur ;
    - supprimer une paire en donnant la clé (la valeur sera supprimée en même temps que la clé) ;
    - chercher si une clé existe dans la table ;
    - retrouver la valeur associée à une clé ;
    - modifier la valeur associée à une clé.

- **Quelles sont les nuances d'un langage à l'autre ?Existe-t-il des contextes (langages, environnements, outils) où elle n'existe pas ?**

- **Quelles sont ses alternatives ?**

    Les listes chaînées sont très flexibles, mais ont un gros défaut lorsqu'on souhaite lire ce qu'elles contiennent : il n'est pas possible d'accéder directement à un élément précis (il faut parcourir la liste pour y accéder).

    Par rapport aux tableaux : on accède grâce au clés et pas aux index ! (plus pratique)

# **Tableau (*array*)**

- **Quel est son rôle ? Quel est son intérêt?**

On stocke les éléments dans des cases, chaque case étant étiquetée d'un numéro (généralement appelé indice). Pour accéder à un élément particulier d'un tableau, on donne son indice.

Les indices sont des entiers consécutifs, et on considérera qu'ils commencent à 0, comme dans la plupart des langages de programmation. Le premier élément est donc à l'indice 0, le deuxième à l'indice 1, etc. (attention au décalage). En particulier, si n est la taille du tableau, le dernier élément se trouve à l'indice n-1

La longueur du tableau est connue par le programmeur

- **A-t-elle des désavantages ?**

On peut accéder efficacement  à un élément du tableau (par son index)

- Mieux de mettre 10 valeurs dans un tableau (une variable), que de créer 10 variables différentes
- Par rapport à la liste : bcp plus difficile d'ajouter et de retirer des éléments (car dans un TABLEAU les éléments sont stockés proches l'un à l'autre dans la mémoire) —> dans un TABLEAU, on ajoute un élément à la fin et il faut faire sort après
- 
- **Y a-t-il plusieurs façons de s'en servir ?**
- **Quelles sont les étapes importantes pour la mettre en place ?**

Dans la plupart des langages, il faut initialiser un tableau (donner une valeur initiale à chacune des cases) pour qu'il fonctionne

**Javascript** 

Création de l'array

je stoque plusieurs valeurs dans une variable

**var cars = ["Saab", "Volvo", "BMW"];**

Accéder aux éléments d'un array

- option 1 : grâce à l'index
- option 2 :

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5dc01771-b1a7-40bd-b8dc-ae5809ae4617/Capture_decran_2021-03-01_a_14.25.54.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5dc01771-b1a7-40bd-b8dc-ae5809ae4617/Capture_decran_2021-03-01_a_14.25.54.png)

    (retourne un objet HTMLElement à partir de son identifiant, défini dans la propriété id de la balise de l'objet —> Ici on veut retourner la valeur d'un élément d'un tableau dans HTML)

- Changer les éléments d'un tableau (on lui assigne tout simplement une nouvelle valeur)

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0395840c-82d9-402b-a397-d586850f180b/Capture_decran_2021-03-01_a_14.32.02.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0395840c-82d9-402b-a397-d586850f180b/Capture_decran_2021-03-01_a_14.32.02.png)

- Accéder à tout l' ARRAY (le visualiser tout sur HTML)
- Les éléments des TABLEAUX en Javascript sont des objets et ont des Propriétés et des Méthodes
    - Exemple : length property

        var fruits = ["Banana", "Orange", "Apple", "Mango"];

        fruits.length;

- **Quelles sont les nuances d'un langage à l'autre ?**

Le tableau est sans doute la structure de données la plus courante, du moins dans les langages dérivés ou inspirés par le langage C

Présent en Javascript, C, C++, Java...

- **Existe-t-il des contextes (langages, environnements, outils) où elle n'existe pas ?**

Pas présent en Python (que listes)

- **Quelles sont ses alternatives ?**

Listes

# **Liste**

- **Quel est son rôle ?**

    **Définition générale :**

    Les listes sont composées d'un ensemble de **cellules** possédant un ou plusieurs **champs.** —> Une cellule est tout simplement un ensemble de cases qui permettent de stocker des données, et auxquelles on accède par leur nom (que l'on appelle nom du champ, comme les champs des formulaires par exemple).

    - Une liste est :
        - soit la liste vide ;
        - soit une cellule à deux champs, un champ `tête` contenant un élément, et un champ `queue` contenant l'adresse d'une autre liste.

    **LE PLUS SIMPLE TYPE DE LISTE DECRITE ICI : la liste chainée** car les cellules contiennent seulement, en plus d'un élément, une flèche vers le suivant (on imagine que ces flèches forment une chaîne).

    - Contient plusieurs **NOEDS** (chaque noed contient une valeur et un **POINTEUR** = une flèche vers l'élément suivant de la liste)

**PYTHON**

À noter que les "listes Python" sont des tableaux dynamiques.

Les listes permettent de rassembler plusieurs valeurs dans une seule structure

C'est une collection d’éléments qui sont

ordonnés

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3f40b73c-b06a-441f-b49d-948c55108d6c/Capture_decran_2021-03-01_a_10.35.11.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3f40b73c-b06a-441f-b49d-948c55108d6c/Capture_decran_2021-03-01_a_10.35.11.png)

modifiables (on peut ajouter et supprimer les éléments même après la création)

répétables

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e0fbf0a4-39c0-47e3-b358-9efe43e916b3/Capture_decran_2021-03-01_a_10.37.38.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e0fbf0a4-39c0-47e3-b358-9efe43e916b3/Capture_decran_2021-03-01_a_10.37.38.png)

- **Quel est son intérêt ?**

With linked lists, your items can be anywhere in memory. Each item stores the address of the next item in the list. A bunch of random memory addresses are linked together. Adding an item to a linked list is easy: you stick it anywhere in memory and store the address with the previous item.

1) On peut ajouter des elements en fin de liste

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/67a47190-31e3-4ca9-b3d2-ba57835216c3/Capture_decran_2021-03-01_a_11.15.28.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/67a47190-31e3-4ca9-b3d2-ba57835216c3/Capture_decran_2021-03-01_a_11.15.28.png)

2) ajouter un element a une position particuliere de la liste

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/365b7201-b98a-4e31-a82d-cc29b218a371/Capture_decran_2021-03-01_a_11.17.48.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/365b7201-b98a-4e31-a82d-cc29b218a371/Capture_decran_2021-03-01_a_11.17.48.png)

3) ajouter des elements d'une autre liste

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0db3707e-6243-4f83-9bfd-f1ce64fc83db/Capture_decran_2021-03-01_a_11.24.40.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0db3707e-6243-4f83-9bfd-f1ce64fc83db/Capture_decran_2021-03-01_a_11.24.40.png)

4) On peut modifier les elements dans une liste en utilisant la meme syntaxe

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e08c55d4-639d-434b-8a12-b69a52f43910/Capture_decran_2021-03-01_a_11.42.51.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e08c55d4-639d-434b-8a12-b69a52f43910/Capture_decran_2021-03-01_a_11.42.51.png)

- **A-t-elle des désavantages ?**
- Le désavantage des listes chaînées est qu'on peut pas accéder super rapidement à un élément du tableau (car pas d'index) — à choisir quand on veut facilement ajouter et supprimer des éléments
- **Y a-t-il plusieurs façons de s'en servir ?**

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/094fe017-a013-49b1-875e-7672200a4724/Capture_decran_2021-03-01_a_10.57.50.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/094fe017-a013-49b1-875e-7672200a4724/Capture_decran_2021-03-01_a_10.57.50.png)

- **Quelles sont les étapes importantes pour la mettre en place ?**

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6adb94eb-afca-41b7-8e8d-db4a87211e4b/Capture_decran_2021-03-01_a_11.05.24.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6adb94eb-afca-41b7-8e8d-db4a87211e4b/Capture_decran_2021-03-01_a_11.05.24.png)

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0b95846a-b93f-452d-a64f-d8372e393f68/Capture_decran_2021-03-01_a_11.05.01.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0b95846a-b93f-452d-a64f-d8372e393f68/Capture_decran_2021-03-01_a_11.05.01.png)

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/26dee7e3-c5f1-4bea-8ab9-6615ed35a17d/Capture_decran_2021-03-01_a_11.04.28.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/26dee7e3-c5f1-4bea-8ab9-6615ed35a17d/Capture_decran_2021-03-01_a_11.04.28.png)

    Une liste peut etre remplie a l'aide de variables et d'operations:

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/78979ae9-9834-4918-96c1-fcabf464e8f9/Capture_decran_2021-03-01_a_11.09.56.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/78979ae9-9834-4918-96c1-fcabf464e8f9/Capture_decran_2021-03-01_a_11.09.56.png)

    Pour designer un element d'une liste, on indique son indice entre crochets []

    *Les n éléments d'une liste sont indexes pas des valeurs de () a n-1.

    *Ces valeurs sont appelées les indices.

- **Quelles sont les nuances d'un langage à l'autre ?**

    en Python on peut utiliser des indices négatifes (pour acceder aux derniers elements de la liste)

- **Existe-t-il des contextes (langages, environnements, outils) où elle n'existe pas ?**

    - les cellules auront des formes différentes : struct en C, objets en Java, etc.

    (Struct en C : structures de données composées, qui peuvent contenir des données très différentes à un seul endroit. Exemple : données bancaires. Souvent on crée un TABLEAU auquel on lie plusieurs STRUCT)

    La plupart des langages de programmation connaissent le concept de TABLEAU (comme en JS). En python le tableau n'existe pas, on manipule des listes.

- **Quelles sont ses alternatives ?**

    tuple, tableaux —> mais le gros avantage des LISTES CHAINEES est qu'on peut les agrandir et réduire en changeant leur POINTER très facilement ! (flexibilité)

# **Tuple**

- **Quel est son rôle ?**

Un tuple est une liste qui ne peut plus être modifiée.

*les operations et fonctions des listes sont accessible egalement pour les tuples (sauf les operations de modification).

- **Quel est son intérêt ?**

On utilisera un tuple pour définir des sortes de constantes qui n'ont donc pas vocation à changer.

- **A-t-elle des désavantages ?**

les elements sont non modifiable

- **Y a-t-il plusieurs façons de s'en servir ?**

- **Quelles sont les étapes importantes pour la mettre en place ?**

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/13217b40-86a3-47ef-b151-d9dbd08d25aa/Capture_decran_2021-03-01_a_11.50.02.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/13217b40-86a3-47ef-b151-d9dbd08d25aa/Capture_decran_2021-03-01_a_11.50.02.png)

- **Quelles sont les nuances d'une structure de donnee à l'autre ?**

le syntaxe est different + la particularite de tulpe avec un seul element c'est que il y a toujour une virgule a la fin

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/917849e0-96cf-443b-b75b-bf5f2031f5b0/Capture_decran_2021-03-01_a_10.41.44.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/917849e0-96cf-443b-b75b-bf5f2031f5b0/Capture_decran_2021-03-01_a_10.41.44.png)

Opérations possibles : appartenance, concaténation entre 2 tuples, indexation, fonctions usuelles (max, somme, taille)

- **Existe-t-il des contextes (langages, environnements, outils) où elle n'existe pas ?**

-Présents aussi en C++, Lisp, Linda

-Pas présents en Javascript !

- **Quelles sont ses alternatives ?**

Les listes (dont l'avantage est qu'elles sont  MODIFIALES) ou les ensembles/sets (non ordonnés et non repétables )

# **Ensemble (*set*)**

- **Quel est son rôle ? Quel est son intérêt ?**

Il s'agit d'une liste : non ordonnée, modifiable et non répétable.

1) **Non ordonnée** - l'ordre n'a pas d'importance :

s1 = {1, 2, 3}

s2 = {3,2,1}

S1 == S2

**TRUE**

- on ne peut pas accéder à un élément  selon son ordre/ un index

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4da6dea8-ac24-498b-bb6e-79c9a9f72884/Capture_decran_2021-03-01_a_11.40.39.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4da6dea8-ac24-498b-bb6e-79c9a9f72884/Capture_decran_2021-03-01_a_11.40.39.png)

2) Modifiables - ajout d'éléments et de collections d'éléments : 

- **ajout d'éléments** ( Pour les LISTES c'était append, ici c'est ADD=⇒ .add)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5338e22a-499d-46a1-af5c-f448ba0707fe/Capture_decran_2021-03-01_a_11.46.04.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5338e22a-499d-46a1-af5c-f448ba0707fe/Capture_decran_2021-03-01_a_11.46.04.png)

couleur rajoutée !

- ajout collection d'éléments (dans liste c'était extend, ici c'est UPDATE)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/aea84110-5d2f-49fc-b909-d3c307f1e4e9/Capture_decran_2021-03-01_a_11.48.39.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/aea84110-5d2f-49fc-b909-d3c307f1e4e9/Capture_decran_2021-03-01_a_11.48.39.png)

IMPLEMENTATION DE LA NOTION D'ENSEMBLE EN MATHEMATIQUE, les opérations sur les ensembles :

- **I (union)**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e9283234-db6e-4504-a577-6d58deed13c2/Capture_decran_2021-03-01_a_11.51.36.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e9283234-db6e-4504-a577-6d58deed13c2/Capture_decran_2021-03-01_a_11.51.36.png)

- Les couleurs présents dans 2 éléments, n'apparaissent qu'une fois

- **& (intersection)**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29a7371f-71b3-4773-9097-6bc2aca88a11/Capture_decran_2021-03-01_a_11.52.46.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29a7371f-71b3-4773-9097-6bc2aca88a11/Capture_decran_2021-03-01_a_11.52.46.png)

- **- (différence)**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/57602bbb-869b-40a8-94f9-de66730ddd9d/Capture_decran_2021-03-01_a_11.54.48.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/57602bbb-869b-40a8-94f9-de66730ddd9d/Capture_decran_2021-03-01_a_11.54.48.png)

Les éléments de l'un moins les éléments de l'autre

- **^ (différence symmétrique = union - intersection**. Dans un référentiel U, la différence symétrique des ensembles A et B est l’ensemble des éléments appartenant soit à A, soit à B, mais pas aux deux ensembles à la fois.)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/56d794bc-2c01-4f75-bc3f-610382a7b0c4/Capture_decran_2021-03-01_a_11.56.37.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/56d794bc-2c01-4f75-bc3f-610382a7b0c4/Capture_decran_2021-03-01_a_11.56.37.png)

3) Non répétables

- Si je crée un tableau avec des éléments écrits en plusieurs fois, dans l'OUTPUT on les verra qu'une fois

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4ad2d4f9-cb37-4e38-af53-25a1e784be9a/Capture_decran_2021-03-01_a_11.42.41.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4ad2d4f9-cb37-4e38-af53-25a1e784be9a/Capture_decran_2021-03-01_a_11.42.41.png)

- **A-t-elle des désavantages ?**

pas d'indexation (non ordonnées)

pas de doublons (non répétables)

- **Y a-t-il plusieurs façons de s'en servir ?**

-Si l'on veut éliminer des doublons d'une LISTE, il peut être pratique de convertir la liste en ENSEMBLE et puis la reconvertir en LISTE

- **Quelles sont les étapes importantes pour la mettre en place ?**

Créer une variable SET, exemple : set1 et lui assigner des valeurs entre accolades

s1 = {1, 2, 3}

- **Quelles sont les nuances d'un langage à l'autre ?Existe-t-il des contextes (langages, environnements, outils) où elle n'existe pas ?**

En Javascript, il existe l'OBJET SET

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/261ba2c7-df5a-4ef4-9b1d-263a5cd5f1aa/Capture_decran_2021-03-01_a_12.15.06.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/261ba2c7-df5a-4ef4-9b1d-263a5cd5f1aa/Capture_decran_2021-03-01_a_12.15.06.png)

- **Quelles sont ses alternatives ?**

Les listes ou les tuples

# Pile (stack*)*

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/01bed903-83e0-427a-8ed4-704982e6fea0/Capture_decran_2021-03-01_a_14.47.21.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/01bed903-83e0-427a-8ed4-704982e6fea0/Capture_decran_2021-03-01_a_14.47.21.png)

- **Quel est son rôle ?**

Pile serve à mémoriser des évènements en attente de traitement. En informatique une pile sert essentiellement à stocker des données qui ne peuvent pas être traitées immédiatement, car le programme a une tâche plus urgente ou préalable à accomplir auparavant. En particulier les appels et retours de fonctions sont gérés grâce à une pile appelée pile d'exécution.

En termes de programmation, une pile est un enregistrement avec :
- Une structure de données pour enregistrées les valeurs (elle peut être statique ou dynamique)
- Une variable sommet qui indique le sommet de la pile.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6c188178-2fbf-4f72-87b4-d517a884b463/Capture_decran_2021-03-01_a_15.44.46.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6c188178-2fbf-4f72-87b4-d517a884b463/Capture_decran_2021-03-01_a_15.44.46.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0f3c9a77-c11c-4090-82f3-4837687ef666/Capture_decran_2021-03-01_a_15.47.40.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0f3c9a77-c11c-4090-82f3-4837687ef666/Capture_decran_2021-03-01_a_15.47.40.png)

- **Quel est son intérêt ?**

Les piles sont basées sur le principe LIFO (Last In First Out : le dernier rentré sera le premier à sortir). Une pile est un ensemble de valeurs ne permettant des insertions ou des suppressions qu’a une seule extrémité, appelée sommet de la pile.

---

Les données enregistrées dans la pile peuvent être des entiers, des réels, des caractères, des chaînes de caractères, des booléens, des tableaux, des pointeurs de listes ou encore des piles ou files.

---

Une **pile statique**: un tableau à hauteur maximale prévisible et un indice entier qui pointe la dernière valeur ajoutée à la pile (sommet).

Une **pile dynamique** est une liste à la quel on attache un pointeur sommet. C’est un enregistrement à une seule case : pointeur qui pointe la dernière valeur traitée dans la liste (sommet).

- **A-t-elle des désavantages ?**

Dans les piles, il est uniquement possible de manipuler le dernier élément introduit dans la pile. On prend souvent l'analogie avec une pile d'assiettes : dans une pile d'assiettes la seule assiette directement accessible et la dernière assiette qui a été déposée sur la pile.

- **Y a-t-il plusieurs façons de s'en servir ?**

    Il y a deux techniques d’implémentation possibles, avec un tableau et avec une liste simplement chaînée.

- **Quelles sont les étapes importantes pour la mettre en place ?**

    La manipulation d’une pile revient à l’appel de fonctions et procédures dites de bases définies une seule fois et utilisées autant de fois qu’il est nécessaire.
    Ces sous-algorithmes sont :
    Init_Pile : permet d’initialiser une pile à vide lors de sa création ;

    Pile_vide : pour vérifier si une pile est vide ou non et savoir alors s’il reste des valeurs à traiter ou non ;
    Pile_pleine : pour vérifier s’il est possible de rajouter ou non un nouveau élément (utilisée dans le seul cas des piles statiques) ;

    Empiler : permet d’ajouter une nouvelle valeur (envoyé en paramètre par l’appelant) à la pile (au dessus du sommet et dans le cas d’une pile non pleine) ;
    Depiler : permet de supprimer une valeur (se trouvant au sommet de la pile) et de la renvoyer en paramètre. Cette opération n’est possible que si la file n’est pas vide.

- **Quelles sont les nuances d'un langage à l'autre ?**

Il n'y a pas de structures spécifiques prévues dans les langages de programmation pour les piles ou files. Il faut donc les créer de toute pièce sachant que la représentation en mémoire de ces structures de données peut être, selon le besoin, statique (utilisation des tableaux) ou dynamique (utilisation des listes).

# File (*queue*)

cela correspond bien à une file d'attente

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/30fe289e-daf7-4c65-98b1-f30b42862ad1/Capture_decran_2021-03-01_a_14.48.38.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/30fe289e-daf7-4c65-98b1-f30b42862ad1/Capture_decran_2021-03-01_a_14.48.38.png)

- **Quel est son rôle ?**

File - une structure de données ordonné.

Serve à mémoriser des choses en attente de traitement. 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c58130d8-06ee-4db4-9340-51d9d1a8fb6c/Capture_decran_2021-03-01_a_15.48.50.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c58130d8-06ee-4db4-9340-51d9d1a8fb6c/Capture_decran_2021-03-01_a_15.48.50.png)

- **Quel est son intérêt ?**

En informatique une file sert essentiellement à stocker des données qui doivent être traitées selon leur ordre d’arrivée. L’exemple le plus connu est celui de l’impression de documents reçus par une imprimante qui imprime le premier document arrivé et termine par le dernier.premier entré, premier sorti (ou FIFO, First In, First Out).

---

En termes de programmation, une file est un enregistrement avec :
- Une structure de données pour enregistrées les valeurs (elle peut être statique ou dynamique)
- Une variable Debut qui indique le premier élément de la file.
- Une variable Queue qui indique le dernier élément de la file.

---

Une **file statique** est un enregistrement à 3 cases : un tableau à hauteur maximale prévisible, un indice entier qui pointe le premier élément insérer dans la file (Debut) et un deuxième indice entier qui pointe la dernière valeur ajoutée (Queue).

Une **File dynamique** est une liste à la quel on attache deux (2) pointeurs Debut et Queue. C’est un enregistrement à deux cases : pointeur qui pointe le premier élément de la liste (Debut) et un autre qui pointe la dernière valeur ajoutée dans la liste (Queue)

- **A-t-elle des désavantages ?**

- **Y a-t-il plusieurs façons de s'en servir ?**

    1) Il y a deux techniques d’implémentation possibles, avec un tableau et avec une liste simplement chaînée.

    2) Il y a trois opérations élémentaires :

    1. tester si la fille est vide
    2. ajouter un élément dans la fille
    3. retirer un élément de la fille (tenter de retirer un élément d’une fille vide déclenche une erreur)

- **Quelles sont les étapes importantes pour la mettre en place ?**

    Comme pour les piles, la manipulation d’une file revient à l’appel de fonctions et procédures dites de bases définies une seule fois et utilisées autant de fois qu’il est nécessaire.
    Init_File : permet d’initialiser une file à vide lors de sa création ;

    File_vide : pour vérifier si une file est vide ou non et savoir alors s’il reste des valeurs à traiter ou non ;
    - File_pleine : pour vérifier s’il est possible de rajouter ou non un nouveau élément (utilisée dans le seul cas des files statiques) ;

    Enfiler : permet d’ajouter une nouvelle valeur (envoyé en paramètre par l’appelant) à la file (après le dernier élément de la file qui se trouve au niveau de sa queue et dans le cas d’une file non pleine) ;
    - Defiler : permet de supprimer une valeur (se trouvant au début de la file) et de la renvoyer en paramètre. Cette opération n’est possible que si la file n’est pas vide.

- **Existe-t-il des contextes (langages, environnements, outils) où elle n'existe pas ?**
- 
- **Quelles sont ses alternatives ?**

# Dèque

- Quel est son rôle ?

Les deques sont une généralisation des piles et des files (double-ended queue) : il est possible d'ajouter et retirer des éléments par les deux bouts des deques. Celles-ci gèrent des ajouts et des retraits utilisables par de multiples fils d'exécution (thread-safe) et efficients du point de vue de la mémoire des deux côtés de la deque, avec approximativement la même performance en O(1) dans les deux sens.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f7e8b93f-44e5-49bf-a628-858464065c0b/Capture_decran_2021-03-01_a_15.50.47.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f7e8b93f-44e5-49bf-a628-858464065c0b/Capture_decran_2021-03-01_a_15.50.47.png)

- **Quel est son intérêt ?**

L'utilisation de deque est préféré à la liste dans les cas où on a besoin d'opérations d'ajout/pop (**Enlève de la liste)** plus rapides et des deux extrémités du conteneur, car deque fournit une complexité de temps O (1) pour les opérations d'ajout et de pop par rapport à la liste qui fournit une complexité de temps O (n) .
