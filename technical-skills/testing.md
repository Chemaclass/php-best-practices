[Back to technical skills](../technical-skills)

# Testing

## Definition

A test is basically the proof of the expected behaviour of your software.

## Common types

### Unit test

- Verify that given an input will expect an output, from a unit perspective.
- A unit is the minimum scope of your code.
- We could agree on a class behaviour or a function itself.
- These tests must be independent of each other.
- They cannot talk to the DB.

### Integration test

- It verifies the behaviour of multiple units together.
- They can talk to the DB.

### Functional / End-to-end / black-box test

- These tests don't care about how but if the ending result of a total is the expected behaviour, without caring at all about any detail implementation.
- They are independent of the DB.
- The importance of these tests is that they are completely agnostic from the software which is running the production result.

## Frameworks

There are plenty of frameworks to write tests, but I will encourage you to first master the most popular one: [PHPUnit](https://phpunit.de/documentation.html). Once you know this one, you will be able to learn any other testing-tool without any problem. Mostly, because almost all of them are based on this one.

## Cohn Pyramid

- The more integrational test -> the slower it will be.
- The more isolated test -> the faster it will be.

## Methodologies

### Test-Last

These tests are implemented after the final/production code was written.

### Test-First

These tests are implemented before start writing the final/production code.

### Test-Driven Development (TDD)

Similar to Test-First, with the important remark that the tests will help you to define and refactor the production code while you are implementing the final result. TDD helps you to design an easily testable code because the production code and its tests are written in parallel.

## References

### Books

* **Testing y TDD para PHP** ([Leanpub](https://leanpub.com/testingytddparaphp/read)) ([Github](https://github.com/franiglesias/testing-php)) [Spanish] by Fran Iglesias
* **Working Effectively with Legacy Code** ([Amazon](https://www.amazon.es/Working-Effectively-Legacy-Robert-Martin/dp/0131177052)) [English] by Feathers Michael

### Medium Posts

* [The Art of Testing: where Design meets Quality](https://medium.com/@chemaclass/the-art-of-testing-39c6af8c9076)
* [The importance of the tests in our software](https://medium.com/@JesusValeraReales/the-importance-of-the-tests-in-our-software-71c6ca020cf6)
