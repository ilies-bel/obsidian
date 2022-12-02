## 1. Qu'est ce que java 

Un language **POO** qui utilise la **JVM**.

## 2. Qu'es ce que spring

C'est un framework Java qui utilise l'inversion de contrôle rendu possible par l'injection de dépendance. L'injection repose sur un système d'annotations AOP.

## 3. Qu'es ce qu'un stream ?

C'est un flux de données consommables permettant de réaliser les opérations courantes de traitement de données.

## 4. Définition de la JVM 
- Java virtual machine 
+ Outil permettant la compilation et le fonctionnement de code Java **sur toutes les plateformes**
+ Optimise la mémoire vive grâce au GC

## 5. Explique moi l'injection de dépendance

Faire schéma au tableau.

## 6. Fonctionnement de la garbage collection

Eden | Survivor1 | Survivor2 | Old Gen

- Le GC nettoie les objet non utilisés 
- Pour cela il vérifie leurs utilisation dans chaque zone
* eden à chaque cycle  Moins souvent dans s1 et encore moins s2, jamais dans old Gen
* Les objets à durée de vie élévé sont transférés dans les zones suivantes
* Une fois le Old Gen plein le GC arrête complètement l'application pour le nettoyer et le défragmenter on appelle cela un "Stop the world"

Rq : STW n'est pas utilsé dans tout les algo de GC
STW rend le tempsd e réponse de l'application imprédictible ce qui peut poser problème.

## 7. Les différents paradigms de programmation

- POO -> Java - POJO
- AOP -> Annotations spring -> Transactionnal
- Fonctionnel -> Streams / Pattern builder 
- Procedural -> Assembleur

## 8. Les nouveautés de Java
	1. Java 8 -> Streams, prog orienté fonctionnel
	2. Java 11 -> Optimisations, ajout sur String.utils
	3. Java 17 -> Sucre syntaxique ( ex switch)

## 9. Maven
Initialement un gestionnaire de package qui est maintenant une suite d'outil permettant de faciliter le dev java

Goals maven ..

## 10. Les principes de la POO

**Commencer par définir :** La POO est un paradigme qui repose sur la manipulation d'objet qui ont des attributs et des méthodes. 

Parler des principes SOLID et donner un exemple à chaque fois et l’intérêt.

-  Single responsibility, chaque méthode ne doit réaliser qu'une seul tâche afin de granulariser les comportement et faciliter leurs ré-utilisabilité .

( J'ai eu un peu de mal pour donner des exemples de l'inversion de dépendance )
Limiter 

## 11. Contrôle d'accès 
A connaitre

## 13. L'API Collection
C'est une API permettant de manipuler des ensemble de données.

Il faut savoir refaire le schéma des interfaces complet. Et connaitre toutes les implémentatiopns d'ArrayList et Set 
( J'ai eu une question que sortedSet )

