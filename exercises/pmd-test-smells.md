# Detecting test smells with PMD

In folder [`pmd-documentation`](../pmd-documentation) you will find the documentation of a selection of PMD rules designed to catch test smells.
Identify which of the test smells discussed in classes are implemented by these rules.

Use one of the rules to detect a test smell in one of the following projects:

- [Apache Commons Collections](https://github.com/apache/commons-collections)
- [Apache Commons CLI](https://github.com/apache/commons-cli)
- [Apache Commons Math](https://github.com/apache/commons-math)
- [Apache Commons Lang](https://github.com/apache/commons-lang)

Discuss the test smell you found with the help of PMD and propose here an improvement.
Include the improved test code in this file.

## Answer

code executer:

```shell
pmd check -f text -R category/java/bestpractices.xml -d /home/arthurlair/Documents/Universite/M2_ILA/ProjGit/VV/commons-collections/src/main/java
```

exemple bad smell obtenu:

```
/home/arthurlair/Documents/Universite/M2_ILA/ProjGit/VV/commons-collections/src/main/java/org/apache/commons/collections4/bag/AbstractMapBag.java:465:	AvoidReassigningParameters:	Avoid reassigning parameters such as 'array'
```

correctif a apporté:

Cette alerte nous indique qu'il ne faut pas redéfinir des variables passées en paramètre. Pour corriger cette mauvaise pratique, on peut parcourir le tableau et effectuer une opération sur chaque élément, ce qui permet de le modifier sans le redéfinir.




