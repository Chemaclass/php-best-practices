# Testing

## Definition

A test is basically the prove of the expected behaviour of your software.

## Common types

### Unit test

* Verify that given an input will expect an output, from a unit persective.
* A unit is the minimum scope of your code.
* We could agree on a class behaviour or a function itself.
* These tests must be independent from each other.
* They can not talk to the DB.

### Integration test

* It verify the behaviour of multiple units together.
* They can talk to the DB.

### Functional / End-to-end / black-box test

* These tests doesn't care about how but if the ending result of a total is the expected behaviour, without caring at all about any detail implementation.
* They are independent from the DB.
* The importance of this tests is that they are completely agnostig from the software which is running the production result.

## Frameworks

There are plenty of frameworks to write tests, but I will encourage you to first master the most popular one: [PHPUnit](https://phpunit.de/documentation.html). Once you know this one, you will be able to learn any other testing-tool without any problem. Mostly, because almost all of them are based on this one.
