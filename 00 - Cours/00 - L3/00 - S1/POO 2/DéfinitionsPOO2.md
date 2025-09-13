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

## 