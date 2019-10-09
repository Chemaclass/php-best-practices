# Immutability

We should encourage immutability because it makes the code more predictable and straightforward. So we can be sure that our data are truths.

## Why immutability?

### Predictability

Mutation hides change, which create (unexpected) side effects, which can cause nasty bugs. When you enforce immutability you can keep your application architecture and mental model simple, which makes it easier to reason about your application.

### Performance

Even though adding values to an immutable Object means that a new instance needs to be created where existing values need to be copied and new values need to be added to the new Object which cost memory, immutable Objects can make use of structural sharing to reduce memory overhead.

###  Mutation Tracking

Besides reduced memory usage, immutability allows you to optimize your application by making use of reference- and value equality. This makes it really easy to see if anything has changed.

## Examples

```php
// Bad
// TODO: ...
```

```php
// Good
// TODO: ...
```

## References:

* [Wikipedia](https://en.wikipedia.org/wiki/Immutable_object)
* [5 benefits of immutable objects](https://hackernoon.com/5-benefits-of-immutable-objects-worth-considering-for-your-next-project-f98e7e85b6ac)
* [Why is immutability so important](https://stackoverflow.com/questions/34385243/why-is-immutability-so-important-or-needed-in-javascript)