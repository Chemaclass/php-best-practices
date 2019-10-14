
# Functions

Functions should be small

## Argument objects

When a function seems to need more than two or three arguments, it is likely that some of those arguments can be wrapped into a class of their own. In such cases, group them within a class:

```php
// Bad
function makeCircle(double $x, double $y, double $radius): Circle;

// Good
function makeCircle(Point $center, double $radius): Circle;
```

## Have no side effects

Side effects are lies. Your function promises to do one thing, but it also does other hidden things. Sometimes it will make unexpected changes to the variables of its own class or do unexpected behaviour. Sometimes it will make them to the parameters passed into the function or to system globals. In either case they are devious and damaging mistruths that often result in strange temporal couplings and order dependencies, or hide some business logic you are missing.

## Command/Query separation

Functions should either do something or answer something, but not both.

## References:

* [Functions | Clean Code, Episode 3](https://cleancoders.com/episode/clean-code-episode-3/show) By Uncle Bob 
* [Medium post](https://medium.com/coding-skills/clean-code-101-meaningful-names-and-functions-bf450456d90c) about meaningful names and functions