# Minimum Scope

## Private | Protected | Public

* `public`: it will be expose to the outside.
* `protected`: only when you are using inheritance, and you want to have them accesible from the child classes.
* `private`: it should not be expose to the outside. To encapsulate code within its minimum scope. 

## Best rule of thumb

Keep to the minimum the scope of your methods and properties.


## Common antipatterns

#### Protected by default

Writing `protected` when there is no inheritance at all. 
> Do not leave `public` or `protected` something unless you know that you will have to expose it to the outside.

