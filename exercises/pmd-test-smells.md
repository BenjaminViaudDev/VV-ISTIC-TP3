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

DetachedTestCase, JUnit4SuitesShouldUseSuiteAnnotation, JUnit4TestShouldUseAfterAnnotation, JUnit4TestShouldUseBeforeAnnotation, JUnit4TestShouldUseTestAnnotation, JUnitSpelling, JUnitTestsShouldIncludeAssert = "Manual intervention"

JUnitTestContainsTooManyAsserts = "Free ride" ou "Eager test" ou "Assertion roulette" car cela peux amener plusieurs cas de test qui sont tester dans un seul test.

JUnitStaticSuite = "Testing private methods" car cela test l'implémentation et non le résultat.

Example :

