[Back to technical skills](../technical-skills)

# Minimum Scope

## Properties and methods

### Public | Protected | Private

* `public`: it will be expose to the outside.
* `protected`: only when you are using inheritance, and you want to have them accesible from the child classes.
* `private`: it should not be expose to the outside. To encapsulate code within its minimum scope. 

### Best rule of thumb

Keep to the minimum the scope of your methods and properties.

## Classes

Reduce the scope visibility to the minimum using the `final` keyword.

When you see a class prefix with the final keyword you will be sure that this class is not extended by any other in the code, which makes it more readable.

You can read more about final classes in [its own page](./final-classes.md)

## Common anti-patterns

#### Protected by default

Writing `protected` when there is no inheritance at all. 

> Do not leave `public` or `protected` something unless you know that you will have to expose it to the outside.

