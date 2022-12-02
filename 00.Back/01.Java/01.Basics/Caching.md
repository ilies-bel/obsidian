Le caching permet le stockage des informations qui sont réutilisés régulièrement.
**On ne s’intéresse au cache que lorsqu'il y a des problèmes de perf**

La loi de paretto voudrais que 80% des données utilisés soient  réutilisable par le cache augementent drastiquement les performances applicatives 

## Les outils utilisés

Chaque coeur de CPU à un cache L1 tandis que le cach L2 est partagé par tout les coeurs

Spécification JSR-107 a.k.a Jcache permet d'uniformiser l'utilisation des caches dans une application Java. 
https://cache2k.org/docs/jcache/1.1.0/apidocs/cache-api/overview-summary.html

Ehcache propose une implémentation de cette norme mais présentes certaines différences dans ses paramètres par défaut 
Javadoc : https://www.ehcache.org/apidocs/3.9.6/index.html

## Analyser l'utilisation du cache applicatif



## Les concepts
Documentation :
https://www.ehcache.org/documentation/3.10/caching-concepts.html


Le cache se présente en 3 tiers : 
- Heap qui est directement dans la [[02.JVM#Fonctionnement d'un processus]]  de Java 
