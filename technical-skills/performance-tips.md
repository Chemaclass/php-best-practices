# Performance tips

## Comparison

Don’t use loose comparison, always be as strict as possible.

```php
// Bad:
if ($a == $b) {/* ... */}

// Good:
if ($a === $b) {/* ... */}
```

## Using fully-qualified function calls

When calling functions in a namespaced context, additional actions are triggered in PHP which result in slower execution. 

```php
// solution 1:
namespace baz;
\foo();

// solution 2:
namespace baz;
use function foo;
foo();
```

## References

* [Optimizing PHP Performance](https://veewee.github.io/blog/optimizing-php-performance-by-fq-function-calls/)
