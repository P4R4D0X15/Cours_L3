# POO2

## L'exécution d'un programme  
Une société d'objets qui communiquent par envoi de messages

## Équation caractéristique (+ explication des termes)   
*  Objet = Etat + Comportement + Identité
	*  Etat = l'état de la mémoire de l'objet à un instant donné
	* Comportement = L'ensemble des messages compréhensible par l'objet
	* Identité = Référence de l'objet 

## Comment se traduit un envoi de message ?   
Il se traduit dans le code source par l'appel d'une méthode sur un objet cible

## Quel est le type d'un objet ?   
Sa classe génératrice

## Qu'est ce qu'un type de données ?   
Ensemble fini de valeurs muni d'opérations applicables sur ces valeurs

## Quels sont les types primitifs en Java?   
**boolean**, **char**, **byte**, **short**, **int**, **long**, **float**, **double**

## Quels sont les types références en Java?   
**classe**, **interface** , **tableaux**

## Qu'est ce qu'un attributs d'instance ?   
Variables permettant d'accéder à une partie de l'état d'un objet

## Comment déclare-t-on un attribut d'instance ?   
```[Access] [Modif] Type ID_Attr ;```

## Quels sont les différents types d'accès en Java ?   
* ```public``` : Accessible partout dans le code source
* ```private``` : Accessible **uniquement** dans la classe ou il est déclaré
* ```protected``` : Accessible partout dans le même paquetage de la classe où il est déclaré
* ```<rien>``` : Accessible dans la classe ou il est déclaré, et par les héritiers de cette classe

## Les différents modificateurs en Java ?   
* ```abstract``` : Spécifique au méthode d'instance, indique que la méthode est abstraite (= Qui n'a pas de corps)
* ```final``` : Indique que l'attribut et/ou la méthode ne peut pas être modifier
* ```<rien>``` : Valeur par défaut, indique que l'attribut et/ou la méthode est modifiable

## Qu'est ce qu'un constructeur ?   
Une procédure d'initialisation des objets

## Comment déclare-t-on un constructeur ?   
```[Access] ID_Classe ([Args]) [ClauseExc] { Corps }```

## Qu'est ce qu' "Instancier" une classe (Concrète) ?   
"Instancier" signifie créer un objet conforme à la au texte de la classe

## Quelles sont les étapes d'instanciation d'une classe ?   
* 1 - Allocation + initialisation standard des champs
* 2 - Évaluation successive des constructeurs de cette classe
* 3 - Retour de la référence

## Qu'est ce qu'une méthode d'instance ?   
Une procédure ou fonction définie dans une classe, pour implanter une partie du comportement des objets de cette classe

## Comment déclare-t-on une méthode d'instance ?   
```[Access] [Modif] Type ID_Meth ([Args]) [ClauseExc] [{ Corps }]```

## Comment sont passés les arguments en Java ?   
**Toujours** par valeur

## Qu'est qu'un paramètre effectif ?   
C'est la variable que l'ont utilise dans un appel de méthode
```U.m(y)``` : Ici Y est le paramètre effectif

## Qu'est qu'un paramètre formel ?   
C'est la variable locale initialisée avec la valeur du paramètre effectif
```void m (int x) {...}``` : Ici X est le paramètre formel

## Qu'est ce que les caractéristiques de classe et comment sont elles déclarées?   
Ce sont les attributs et les méthodes liés à la classe uniquement, indépendamment de ses instances. Elles sont déclarées avec le mot clé ```static```

## Qu'est ce qu'un Tableau simple ?   
C'est un tableau à une seule dimension
* 1 - ```int [] t;```
* 2 - ```t1 = new int [2]```
* 3 - ```for(int i = 0; i < t1.length; i++) { t1 = 2 * (i + 1); }```
* OU alors en une seule ligne : ```int [] t1 = new int [] {2, 4};```

## Qu'est ce qu'un tableau à n dimensions ?  
C'est un tableau simple de tableaux à n - 1 dimensions
* 1 - ```int[][] t2;```
* 2 - ```t2 = new int[2][];```
* 3 - ```for (int i = 0; i < t2.length; i++) {
		t2[i] = new int[i + 1];
		for (int j = 0; j < t2[i].length; j++) {
			t2[i][j] = i + j + 1;
		}
	 }```
* OU alors en une seule instruction : ```int[][] t2 = new int[][] {
								{ 1 }, { 2, 3 }
							};```

## Qu'est ce qu'un effet de bord ?   
Un effet de bord est une modification de l'état d'un objet dont la valeur référence de celui-ci est passé en paramètre de la méthode qui le modifie

## Les boucles For étendue   
Elles sont utilisables:
* sur un tableau
* lors d'un parcours en lecture de ce tableau
Ce type de boucles sont de la forme:
```for ([final] Type ID_Var : Exp)```
* Exp => est une expression de type ```T[]```
* Type => est un type compatible/conforme avec ```T```

## Le type ```enum```   
Classe (Synthétisée) possédant un nombre fixe d'objets, définis au chargement de la classe, chacun accessible publiquement par une constante statique de ce type

## Qu'est ce qu'une classe enveloppante ?   
C'est une classe qui réifie l'un des 8 types primitifs:
* boolean -> Boolean
* byte -> Byte
* short -> Short
* int -> Integer
* long -> Long
* char -> Character
* float -> Float
* double -> Double

## Qu'est ce que le boxing ?   
Une conversion automatique d'une valeur primitive en une instance de la classe enveloppante appropriée

## Qu'est ce que l' Unboxing ?   
Une conversion automatique inverse d'un Boxing

## Qu'est ce qu'une panne logicielle ?   
Une situation anormale pendant l'exécution, 
provoquant la fin abrupte d'une instruction, 
avec déclenchement d'une exception (**levée d'exception**) ou d'une erreur
qui est transmise en remontant la pile des appels

## Qu'est ce que l'héritage ?   
Un mécanisme permettant de définir un nouveau type (**héritier**)
à partir d'un ou plusieurs autres types (**parents**), en ne codant que les différences entre l'**héritier** et ses **parents**

## Qu'est ce qu'une relation d'héritage ?   
Une relation entre classes. Elle n'intervient pas au niveau des objets qui ont, évidemment, accès à la totalité du code

## Qu'est ce que la conformité entre les types Java ?   
* Elle est basée sur la relation de sous-typage Java
* S est dit **conforme** à T si l'expression ```v = e;``` est légale quand ```v``` est de type T et ```e``` est de type S

## Qu'est ce qu'une Expression ?   
Une formule bien formée à partir de parenthèses, de littéraux, de noms de variables, d'opérations et de noms de méthodes

## Qu'est ce que l'Évaluation d'une expression ?   
La production d'une valeur,
résultant du calcul de cette expression par la JVM,
à un moment donné d'une exécution du programme

## Quels sont les trois types de résultats résultant d'une évaluation d'une expression ?   
* Une zone mémoire (expression ne pouvant aller à gauche ou à droite dans une affectation)
* une donnée (expression ne pouvant aller qu'à droite dans une affectation)
* Rien (pas de résultat), **Appel d'une méthode ```void```**

## Qu'est ce qu'une Valeur d'une expression ?   
La valeur du résultat (quand il existe) du calcul effectué lors de l'évaluation de l'expression

## Quelles sont les étapes de l'évaluation d'une affectation par la JVM ?   
1. Évalue la sous-expression de droite
2. Évalue la sous-expression de gauche
3. copie la valeur obtenue dans la zone mémoire (effet de bord)
La valeur d'une expression d'affectation est la valeur de son expression de droite

## Le type d'une expression (**Type Statique**)   
Le type calculé sur la base de :
* littéral  -> type du littéral, défini par le langage
* Opérateur -> type de la valeur produite, défini par le langage
* variable -> type de la variable, déclaré dans le code
* appel de méthode (non void) -> type de retour, déclaré dans le code 
Le type statique ne peut pas varier au cours du temps

## Type de la valeur d'une expression (Type Dynamique)
* Valeur primitive -> Type Statique de l'expression
* Valeur référence -> classe génératrice de l'objet
Le type dynamique d'une expression peut varier au cours du temps

## L'Opérateur ```instanceof```   
Détermine, pendant l'exécution, si la valeur d'une expression est une instance du type indiqué

## Qu'est ce que le Transtypage (```cast```) ?   
C'est le remplacement du type d'une expression par un autre type, à l'aide d'une opération de cast ```(ID_Type) e```

## Qu'est ce que l'Extensibilité potentielle ?   
Quand S et T ne sont pas en relation de sous-typage, S est potentiellement extensible en un type conforme à T s'il **pourrait** exister à l'exécution un sous-type propre de S et T

## Qu'est-ce que le masquage d'attribut (ou de méthode de classe) ? :
La Redéclaration dans une sous-classe d'un attribut (accessible) de sa super-classe masque (dans la sous-classe) l'attribut de la super-classe

## Quelle est la règle de résolution d'accès ? 
Le type de l'expression cible qui détermine l'attribut auquel on accède

## Qu'est ce qu'une Redéfinition de Méthode ? 
Le remplacement du corps d'une méthode d'instance (concrète) lors de l'héritage

## Que signifie le terme "@Override" ?
Il permet de vérifier que l'on fait bien une redéfinition

## Qu'est ce que le Surchage de méthode (ou "polymorphisme d'Ad'hoc") ?
La déclaration de plusieurs méthodes ayant même nom mais de signature différente

## Quels sont les 4 cas possible de l'Invocation de méthode ?
* Méthode d'instance, cas classique (liaison dynamique)
* Méthode d'instance, privée (liaison statique)
* Méthode d'instance, appelée avec super (liaison statique)
* Méthode de classe, (liaison statique)

## Comment l'invocation de méthode fonctionne dans un cas de surcharge
Le compilateur va chercher le plus petit type (Dans le sens d'une relation de sous-typage) tel que W est un sous-type de X et que la signature de la méthode  m existe dans le type statique de la variable qui appelle une méthode surchargé

## Qu'est ce que l'Ambiguïté en Java ?
$min \{(X_1, ... ,X_n)\}$ n'existe pas toujours (voir l'algorithme sur l'invocation en présence de surcharge Diapo 47 cm6)

## Qu'est ce qu'un paquetage Java? Quels sont ses avantages ?
C'est une unité de regroupement de types et de sous-paquetages en un tout logiquement cohérent
* Meilleure gestion du code
* Fournit un espace de nommage
* Fournit un niveau supplémentaire de masquage de l'information
* **Un paquetage est toujours accessible**

## Quels sont les différentes accessibilités pour un type ($B \in p$)?
* public -> accessible dans tout type
* ```<rien>``` -> accessible seulement dans le même paquetage

## Quels sont les différentes accessibilités pour un caractéristique $c \in B (B \in p)$?
* public -> accessible seulement dans les cas où $B$ est accessible
* protected -> accessible dans le même paquetage **et** dans les sous-types de $B$ **et** "**qui sont responsable de l'implémentation de l'objet cible de l'appel**" (this / super / tq TS(x) sous-type de T (T <: $B$))
*  ```<rien>``` -> accessible seulement dans le même paquetage
* private -> accessible que dans $B$

## Qu'est ce qu'un Flux ?
Objet transportant des données séquentiellement et en quantité indéterminée, et qui permet une communication standardisée entre le programme et son environnement 

## Quels sont les 3 axes de classifications des flux ?
1. Selon le mode d'accès aux données (lecture / écriture)
2. Selon le type des données transportées (textuelles/ binaires)
3. Selon le mode opératoire (primaire / traitement)

## Qu'est ce que l'encapsulation de données ?
Une technique dans laquelle des opérations sémantiquement reliées qui sont regroupées au sein d'un même élément logiciel, avec les structures de données utilisées pour leur implémentation

## Qu'est ce que la Rétention d'information ?
Possibilité de masquer aux clients d'un élément logiciel toutes les parties de son code qui sont sans intérêt pour les clients, à l'aide d'un mécanisme d'accès sélectif défini au niveau du langage

## Qu'est ce que le principe d'encapsulation ?
Seul l'objet lui-même à accès à ses propres informations

## Qu'est ce qu'un module ?
Élément logiciel résultant de l'abstraction d'un concept, réalisé en suivant le principe d'encapsulation

## Qu'est ce qu'un TDA (Type de données Abstrait) ?
* Ensemble d'éléments muni d'opérations
* Défini par une spécification qui exprime la sémantique des opérations

## Qu'est ce qu'une fonction partielle ?
$E_{def} \subset E_{départ}$ (noté "-/->")

## Qu'est ce qu'une fonction Totale ?
$E_{def} = E_{départ}$ (noté "-->")

## Qu'est ce qu'une requête ? Quels sont les deux types de requêtes ?
Permet d'accéder à la description du TDA :
* Requête de Base : Requête "indispensable" au bon fonctionnement du TDA
* Requête Dérivée : Requête calculable à partir des requêtes de Base

## Qu'est ce qu'un générateur ? Quels sont les deux types de générateurs ?
Permet d'accéder au TDA :
* Créateur : Accès au TDA à partir d'une valeur externe
* Commande : Accès au TDA à partir d'un autre objet de ce même TDA

## Qu'est ce que la programmation par contrat (B. Meyer) ?
Une méthode de construction du logiciel qui conçoit les composants d'un système de telle façon qu'ils coopèrent sur la base de contrats définis de façon formelle

## Qu'est ce qu'un contrat ?
Une spécification de constructeur ou de méthode qui en définit les conditions de bonne utilisation ainsi que l'effet produit par son exécution

## Qu'est ce qu'un Invariant de Type ?
Une spécification à l'état observable de toutes les instances d'un même type lorsqu'elles sont en phase stable

## Qu'est ce qu'une classe correcte ?
Une classe qui doit :
* respecter sa spécification, données par un TDA
* être codée comme un module

## Qu'est ce que la Méthode ```equals``` ?
Réalise une d'équivalence sur les objets (Utilisée surtout pour les collections)

## Quel est le Contrat de la Méthode ```equals``` ?
```
@pre : true
@post : Équivalence + Consistante + Compatible avec null
```

## Qu'est ce que la Méthode ```HashCode``` ?
Représente une fonction de dispersion sur les objets, utilisée dans les tables de hachages internes à certain types de collections

## Quel est le Contrat de la Méthode ```HashCode``` ?
```
@pre : true
@post : Consistante avec, et domination par equals
```

## Qu'est ce que la Règle de consistance avec ```equals``` ?
Tant que les données utilisées par ```equals``` ne varient pas la valeur retournée par ```hashCode``` ne change pas

## Qu'est ce que la Règle de domination par ```equals``` ?
```x.equals(y) => x.hashCode() == y.hashCode()```

## Qu'est ce que ```Clone``` ?
Créer et retourne une copie d'un objet
## Quel est le Contrat de la Méthode ```Clone``` ?
```
@pre : true
@post : 
	1. l'objet et son clone ne sont pas le même objet
	2. l'objet et son clone sont equals
	3. la classe de l'objet et celle de son clone sont identiques
```

## Qu'est ce que le Principe de Substitution de Liskov (PSL) ?
Pour deux types S et T, si :
* Dans tout programme P, on peut utiliser une valeur de S partout où une valeur de T est attendue, sans modifier le sémantique de P, alors S $\subset$ T (S est sous-type de Liskov de T)

## Quels sont les Avantages de la généricité sur le polymorphisme de sous-typage ?
1. Renforce le typage
2. améliore la sûreté du typage
3. améliore la lisibilité du code

## Qu'est ce qu'un type paramétré ( = instance générique d'un type générique) ?
L'un des éléments d'un type générique, obtenu en substituant à chaque variable de types références références disponibles

## Qu'est ce qu'un type générique ? 
Famille de types, basée sur une unique définition de type, paramétrée par une ou plusieurs variables (ou paramètres) de types

## Qu'est ce que l'effacement de la généricité ?
Le compilateur supprime de bytecode toute information relative à la généricité

## Qu'est ce qu'un Type Brut ?
* Équivaut au type de base d'un type générique
* C'est le seul type présent dans le bytecode, où il remplace à la fois le type générique et tous ses types paramétrés

## Quand est-ce que l'accès aux paramètres de types est impossible ?
Dans le contexte statique d'un type générique

## Comment se fait l'accès aux éléments de type statique d'un type générique ?
Par le type Brut

## Quelle est la règle de Compatibilité Verticale ?
Soient $G<E>$  et $H<E>$ tels que $G<E>$  hérite de $H<E>$ alors $\forall$ A (type référence), $G<A>\ <:\ H<A>$ 

## Quelle est la règle d'Incompatibilité Horizontale ?
Soit $G<E>$ un type générique alors $\forall$ A,  $\forall$ B (types références), ~~G\<A> \<: G\<B>

## Que peut-on dire du Transtypage vers un type paramétré ?
L'instruction ```checkcast``` porte sur le type brut

## Quand est-ce que le compilateur émet l'avertissement ```unchecked``` ?
Quand on ne peut pas garantir que le paramètre de type est correct

## Qu'est ce qu'une Méthode Pont ?
Méthode synthétisée par le compilateur lorsqu'il se produit un changement de signature (à cause de l'effacement de la généricité)
au cours de l'héritage d'une méthode 

