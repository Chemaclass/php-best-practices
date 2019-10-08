# Minimum Scope

## Private VS Protected VS Public

* Make them `public` when you want them to be exposed from the outside.
* Make them `protected` when you are using inheritance, and you want to have them accesible from the child classes.
* Make them `private` to encapsulate code within its minimum scope; for code that it should not be expose to the outside. 

## Common antipatterns

### Protected by default

Write `protected` when there is no inheritance at all. 
> Do not leave `public` or `protected` something unless you know that you will have to expose it to the outside.

## Best rule of thumb

* Keep the scope of your properties and methods always as to the minimum. Always keeping in mind the context of the code.
