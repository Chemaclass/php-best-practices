# Strict types

### Declare strict_types constant when possible

```php
<?php declare(strict_types=1);
// ...
```

The good think about declaring a PHP file as strict is that it applies actually to **ONLY** the current file. 
It ensures that this file has strict types. It doesn't apply to any other file in the whole project. 
It allows you to do, step by step, this migration from non-strict to strict code. Especially for new files or projects.

### Strict types affect type coercion

Using type hints without strict_types may lead to subtle bugs.
Prior to strict types, `int $x` meant "`$x` must have a value coercible to an `int`". 
Any value that could be coerced to an `int` would pass the type hint, including:

* an `int` proper (42)
* a `float` (13.1459)
* a `bool` (true)
* a `null`
* a `string` with leading digits ("15 Trees")

By setting `strict_types=1`, you tell the engine that `int $x` means "`$x` must only be an `int` property, no type coercion allowed." 
You have the great assurance you're getting exactly and only what was given, without any conversion and potential loss.

### Who should care about this "strict type" line?
Actually, `declare(strict_types=1);` is more for the reader than for the writer. Why? 
Because **it will explicitly tell the reader that the types in this current scope (file) are treated strictly**.
The writer just needs to maintain such strictness while writing the expected behavior.

#### "strict_types=1" is more for the reader than for the writer.

## References

* [What do strict types do in PHP?](https://stackoverflow.com/q/48723637/3454593)
