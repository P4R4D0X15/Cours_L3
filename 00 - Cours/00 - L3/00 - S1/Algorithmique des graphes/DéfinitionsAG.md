## Qu'est ce que le degré d'un sommet d'un graphe ?
Le nombres d'arêtes (d'arcs) qui sortent de ce sommet

## Qu'est ce qu'un chemin ?
Une suite d'arêtes consécutives

## Qu'est ce qu'un Graphe non orienté ?
Un Couple $G = <S, A>$ où
* S est l'ensemble fini de sommets
* A est l'ensemble fini de paires de sommets, appelés arêtes

## Qu'est ce qu'un Graphe orienté ?
Un Couple $G = <S, A>$ où
* S est l'ensemble fini de sommets
* A est l'ensemble fini de couples de sommets, appelés arcs

## Qu'est ce qu'un Graphe valué ?
Un Triplet $G = <S, A, p>$ où
*  $G = <S, A>$ est un graphe orienté ou non
* $p$ est une fonction de $A$ dans $\mathbf{R}$, appelée fonctions de poids ou fonction de coût

## Quels sont les deux types de Graphes particuliers ?
* Graphes discrets : $G_0 = <S , \emptyset>$ 
* Graphes complets à n sommets : Graphes non orienté contenant une arêtes pour chaque ensemble de deux sommets

## Qu'est ce qu'une Matrice d'adjacence $M = M(G)$ ?
La matrice carrées de booléens de taille n x n telle que $$M[i, j] =
\left\{
    \begin{array}{ll}
        1 & \mbox{si } \{i,j\} \in A \\
        0 & \mbox{sinon.}
    \end{array}
\right.
$$

## Qu'est ce que la Matrice des distances $D = D(G)$?
La matrice carrée des réels de taille n x n telle que $$D[i, j] =
\left\{
    \begin{array}{ll}
        p(i, j) & \mbox{si } \{i,j\} \in A \\
        + \infty & \mbox{sinon.}
    \end{array}
\right.$$

## Qu'est ce que la Liste des successeurs (de voisins dans le cas d'un graphe non orienté)?
Un tableau ou un liste de longueur n tel que $$Succ=(q_1,...,q_n)\ \ (resp. Vois=(q_1,...,q_n))$$
où $q_i$ est un pointeur sur la liste des successeurs (resp. voisins) du sommet i

## Qu'est ce que la liste d'arcs ou d'arêtes ?
Une liste de la forme : $$<(i, j)> \forall (i,j) \in A$$

## Qu'est ce que l'Accessibilité ?
L'Existence d'un chemin entre deux sommets

## À quoi correspondent x et y dans la notation (x, y) (pour les graphe orienté) ?
* x est l'extrémité initiale 
* y est l'extrémité finale

## Quand dit-on que deux arcs sont Consécutifs ?
Si l'extrémité finale d'un arcs est l'extrémité initiale d'un second arcs

## Quand dit-on que deux arcs sont Adjacents ?
Si ils ont une extrémité en commun 

## Qu'est ce qu'un Chemin de longueur $k$ ?
une suite de $k$ arcs (resp. arêtes) consécutifs 2 à 2

## Qu'est ce qu'une Chaîne de longueur $k$ ?
Une suite de $k$ arcs () adjacents 2 à 2

## Qu'est ce qu'un Circuit de longueur $k$ ?
Une suite de $k$ arcs (resp. arêtes) consécutifs

## Qu'est ce qu'un Cycle de longueur $k$ ?
Une suite de $k$ arcs (resp. arêtes) adjacents

## Qu'est ce qu'un Chemin ou Chaîne "Trivial(e)" ?
Un Chemin ou Chaîne de longueur 0

## Qu'est ce qu'une Boucle ?
Un Cycle ou Circuit de longueur 1

## Qu'est ce qu'un Chemin (resp. Chaîne) élémentaire ?
Un Chemin (resp. une Chaîne) qui ne passe pas deux fois par le même sommet

## Qu'est ce qu'un Circuit (resp. Cycle) élémentaire ?
Un Circuit (resp. Cycle) dont le chemin (resp. chaîne) obtenu(e) en retirant le dernier arc (resp. sommet) est élémentaire

## Comment est l'Ensemble des chemins d'un Graphe orienté?
Il est infini => impossible d'en produire un algorithme 

## Comment est l'Ensemble des chemins Élémentaires d'un Graphe orienté ?
Il est toujours fini => Candidat idéal pour un algorithme

## Qu'est ce qu'un chemin extrait ?
Un chemin extrait d'un chemin $C$ est un chemin $C'$ tel que 
* $C'$ a les mêmes extrémités de $C$
* La suite des sommets de $C'$ est une sous-suite de la suite de sommets de $C$

## Que dit le "Lemme de König" ?
Dans un Graphe orienté $G = <S, A>$, d'un chemin $C$ de $x$ vers $y$, on peut toujours extraire un chemin élémentaire

## Qu'est ce qu'une Matrice d'Accessibilité ?
Une Matrice $AC$ décrite : $$AC[x, y] =
\left\{
    \begin{array}{ll}
        1 & \mbox{s'il existe un chemin de x vers y} \\
        0 & \mbox{sinon}
    \end{array}
\right.$$

## Qu'est ce que le Niveau du chemin ?
Le Niveau d'un chemin $C = (x_0, ... , x_k)$ est défini : $$Niveau(C) =
\left\{
    \begin{array}{ll}
        Max(x_1,...,x_{k-1}) & \mbox{si } k \geq 2 \\
        0 & \mbox{sinon}
    \end{array}
	\right.$$

## Qu'est ce que les Sommets intérieurs d'un chemin $C=(x_0,...,x_k)$ ?
Les sommets $x_1,..., x_{k-1}$

## Comment est définit le Poids d'un chemin $C = (x_0,...,X_k)$ ?
$$p(C) = 
\left\{
	\begin{array}{ll}
		0 & \mbox{si } k = 0 \\
		\sum_{i=1}^k p(x_{i-1},..., x_i) & \mbox{sinon}
	\end{array}
\right.$$

## Qu'est ce qu'un plus court chemin de $x$ vers $y$ ?
Un Chemin de $x$ vers $y$ de poids minimum

## Qu'est ce que la plus courte distance de $x$ vers $y$ ? Comment est-elle notée ?
Le poids d'un plus court chemin de $x$ vers $y$ 

## Qu'est ce qu'un Circuit absorbant ?
Un Circuit de $G$ dont le poids est strictement négatif

