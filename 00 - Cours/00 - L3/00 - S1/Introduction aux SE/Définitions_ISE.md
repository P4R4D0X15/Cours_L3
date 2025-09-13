## Qu'est ce qu'un système d'exploitation ?
Un logiciel intermédiaire qui remplit deux fonctions principales:
* Assurer la **gestion efficace des périphériques matériels**
* Offrir aux programmes une **interface abstraite et simplifiée** pour interagir avec le matériel, sans en connaître les détails techniques

## Quels sont les types de systèmes d'exploitations ?
* Mainframes : traitement de très gros volumes de données
* Serveurs : gestion de services réseaux
* Multiprocesseurs : exploitation de plusieurs CPU en parallèle
* Personnels : ordinateurs individuels
* Temps réel : respect de délais stricts, applications critiques
* Embarqués : systèmes pour les appareils spécifiques
* Cartes à puce : ultra-léger et sécurisés

## Qu'assure la gestion des processus ?
* Création/exécution/ terminaison d'un processus
* Une utilisation optimale du CPU
* Synchronisation & Communication inter-processus
* Isolation et la sécurité entre les applications

## Que permet le systèmes de fichiers ?
* Structurer
* Sécuriser
* Optimiser les accès 

## Qu'est ce qu'une interruption ?
Un évènement asynchrone envoyé au processeur pour indiquer qu'un évènement prioritaire nécessite une attention immédiate. Elle peut être matérielle ou logicielle

## Qu'est ce qu'un appel système ?
Un mécanisme permettant à un programme en mode utilisateur d'accéder aux services du noyau

## Qu'est ce que le mode Utilisateur ?
* L'espace où s'exécutent les applications. 
* Il a un accès limité aux ressources matérielles. 
* Il protège contre les erreurs utilisateurs

## Qu'est ce que le mode Noyau ?
* L'espace privilégié pour le système d'exploitation
* Il a un accès direct aux matériels
* Il gère les appels système et les interruptions

## Qu'est ce qu'un programme binaire ?
Un fichier contenant des instructions exécutables, compilées à partir d'un code source

## Quelles sont les différentes sections d'un programme binaire et quelles sont leurs rôles?
* En-tête : Métadonnées
* .text : Code machine exécutables du programme
* .data : Données initialisées
* .rodata : Données en lecture seule (Constantes)
* .bss (Block Started by Symbol) : Données non initialisées 
* .symtab : Table des symboles pour le "linkage" (références fonctions/ variables)
* .strtab : Table des chaînes de caractères

## Qu'est ce qu'un processus ?
Une instance d'un programme binaire en cours d'exécution

## Quels sont les composants principaux d'un processus ?
* Bloc de Contrôle de Processus 
* Espace mémoire
	* Code : instructions du .text
	* Pile : Stocke les variables locales / appels de fonctions
	* Tas : Mémoire allouée dynamiquement pendant l'exécution
	* Données : Variables statiques (.data et .bss)

## Quels sont les états d'un processus sous Linux ?
* R : Running ou Ready (s'exécute ou prêt à s'exécuter)
* S : Sleeping (Attente interruptible)
* D : Uninterruptible sleep 
* T : Stopped 
* Z : Zombie (fini mais non récupéré par le parent)
* I : Idle (Spécifique au noyau)

## Qu'est ce qu'un Démon (daemon) ?
Un processus qui veux s'exécuter en arrière-plan et se détacher du terminal

## Qu'est ce que le recouvrement d'un processus ?
* Le remplacement de son image mémoire par un nouveau programme
* Réalisé via la familles d'appels système ```exec```
* Utiliser pour exécuter un nouveau programme dans le contexte du processus actuel, en conservant la même entrée dans la table des processus

## Qu'est ce que l'ordonnancement ? 
C'est ordonner l'exécution des programme par ordre de priorité. Cette ordre est appliqué par l'ordonnanceur

## Quand faut-il ordonnancer ?
* Création d'un nouveau processus : Pour savoir s'il doit être exécuté immédiate ou placé en attente
* Fin d'un processus : libération du processus , un autre doit être choisi
*  Blocage d'un processus sur une E/S : CPU disponible pour un autre processus
* Lors d'une interruption

## Qu'est ce qu'un Ordonnancement non préemptif ?
Une fois choisi le processus garde le processeur jusqu'à ce qu'il se termine ou se bloque

## Qu'est ce qu'un Ordonnancement préemptif ?
* Le processus ne garde le processeur que pour un temps limité
* Quand ce temps est terminé, l'ordonnanceur peut choisir un autre processus quelque soit l'état du premier
* Meilleure réactivité et partage du CPU

## Quels sont les trois types principaux de processus sous Linux ?
Processus : 
* Interactifs (attente d'interaction avec les E/S, réponse rapide, ordonnancement préemptifs)
* de traitement (fonctionne en tache de fond, ordonnancement non préemptif ou préemptifs à long délais, maximise le débit, minimise le temps d'attente, processeur occupé en permanence)
* Temps réel (Exigent ordonnacement précis, traités rapidement, réponse prévisible, ordonnancement préemptifs ou non)

## Quels sont les 4 types de politiques d'ordonnancement ?
* Premier arrivé premier servi (FCFS <=> FIFO)
* Job le plus court en premier (SJF)
* Tourniquet (Round Robin)
* Par priorité

## Sous Linux, quel est le type de politiques d'ordonnancement utiliser ?
Les processus sont organiser par niveau de priorités (Statiques et dynamiques)

test