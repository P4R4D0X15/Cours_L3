
## Qu'est-ce q'un Alphabet?
Un ensemble fini de symboles (Noté: a, b)

## Qu'est ce qu'un mot?
Une suite fini de symboles (éventuellement vide) (Noté : w, v, u)

## Qu'est-ce qu'un langage?
Un ensemble de mots (Noté : $\Sigma$ )

## Comment note-t-on le mot vide?
Avec le symbole $\varepsilon$ (Epsilon)

## Quelles sont les propriétés de l'opération de concaténation ?
* Associativité
* Possède un élément neutre : Le mot vide $\varepsilon$

## Qu'est ce que le facteur d'un mot ? préfixe ? suffixe ? facteur propre ?
On dit que f est un facteur de w s'il existe deux mots u et v tels que w = u . f . v
Si u = $\varepsilon$ alors f est un préfixe
Si v = $\varepsilon$ alors f est un suffixe
Si u ou v sont différents de $\varepsilon$ alors f est un facteur propre de w

## Qu'est ce qu'un sous-mots?
Une suite extraite d'un mot w

## Qu'est ce que le miroir d'un mot ?
Le renversé de la suite de lettres qui compose un mot
Exemple : $\vec{abca}$ = $acba$
De plus si $\vec{u}$ = $u$ on dit que u est un palindrome

## Que nous dit le Lemme sur le miroir d'un mot ?
Soit 2 mots $u$ et $v$. On a $\vec{u.v}$ = $\vec{u}$.$\vec{v}$

## Qu'est ce que le complémentaire d'un langage ?
Soit $L$ un langage sur l'alphabet $\Sigma$ ,  $\overline{L}$ est l'ensemble de tous les mots n'appartenant pas à $L$

## Qu'est ce que la copie-ième d'un langage ?
Soit $L$ un langage sur l'alphbet $\Sigma$, $$L^i = L . L^{i-1}$$

## Qu'est ce que l'opération **étoile** ?
Soit $L$ un langage sur l'alphbet $\Sigma$, $$L^* = \bigcup^{\infty}_{i = 0}{L^i}$$

## Qu'est ce que la fermeture positive d'un langage ?
C'est l'opération étoile mais en commençant par 1. En d'autre terme $$L^* = \bigcup^{\infty}_{i = 1}{L^i}$$ Conventionnellement $\emptyset^* = \{ \varepsilon \}$
## Qu'est ce que la différence ensembliste entre deux langages ?
Soit $L_1, L_2$ deux langages sur l'alphbet $\Sigma$, $$L_1 \textbackslash L_2 = L_1 \cup \overline{L_2} $$ 
## Qu'est ce que le quotient à gauche de deux langages ?
Le quotient à gauche de $L_2$ par $L_1$ est défini par $$L_1^-1L_2 = \{v \in \Sigma^* | u.v \in L_2 \land u \in L_1\}$$
## Qu'est ce que le quotient à droite de deux langages?
Le quotient à gauche de $L_2$ par $L_1$ est défini par $$L_1L_2^-1 = \{v \in \Sigma^* | u.v \in L_1 \land v \in L_2\}$$

## Qu'est ce qu'un AFN ?
Un Automate à nombres finis d'états

## Comment est défini formellement un automate ?
C'est un quintuplet ($\Sigma$, $Q$, $I$, $F$, $\delta$ ) :
* $\Sigma$ : un alphabet fini
* $Q$ : un ensemble fini d'états
* $I$ : l'ensemble des états initiaux ($I \subset Q$)
* $F$ : l'ensemble des états finaux ($F \subset Q$)
* $\delta$ : ensemble des transitions

## Qu'est ce qu'une transition et comment est-elle représentée formellement ?
Une transition représente le passage d'un automate d'un état à un autre.
Elle est représenté par un triplet ($e_1 (\in Q), lettre (\in \Sigma), e_2 (\in Q)$)

## Quand dit-on que deux transitions sont consécutives ?
$(p, a_i, q)$ et $(p', a_j, q')$ sont dites *consécutive* ssi $q=p'$

## Qu'est ce que l'ensemble des chemins ?
Une suite de transitions consécutives

## Qu'est ce que la longueur d'un chemin ?
Le nombre de transitions qui composent ce chemin

## Qu'est ce que la trace (label / étiquette) d'un chemin ?
La concaténation des lettres de chacune des transitions consécutives

## Qu'est ce qu'un chemin réussi ? Quand est-il de son étiquettes ?
Un chemin d'étiquette w qui mène d'un état initial à un état final. L'étiquette w est un mot accepté par l'AFN

## Qu'est ce qu'un langage accepté / reconnu par un AFN ?
L’ensemble des mots accepté par cet automate. On le note L(M)

## Que signifie la notation Rec($\Sigma^*$) ?
L'ensemble des langages reconnaissables sur l'alphabet $\Sigma$

## Que signifie la notation AFN($\Sigma^*$)?
L'ensemble des automates sur l'alphabet $\Sigma$

## Quelle la propriété qui est vérifiée entre les deux ensemble Rec($\Sigma^*$) et AFN($\Sigma^*$) ?
La surjectivité

## Qu'est ce qu'un langage reconnaissable ?
Un langage $L$ est reconnaissable s'il existe un AFN sur $\Sigma$ tel que $L=L(M)$

## Qu'est ce qu'un algorithme standard?
Un AFM M est standard s'il possède un état initial **unique non ré-entrant**