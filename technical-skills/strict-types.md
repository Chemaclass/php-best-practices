# Strict types

### Declare strict_types constant when possible

```php
<?php declare(strict_types=1);
// ...
```

In December 2015, PHP 7 introduced [scalar type declarations](https://www.php.net/manual/en/migration70.new-features.php#migration70.new-features.scalar-type-declarations) 
and with it the strict types flag.

> To enable the strict mode, a single declare directive must be placed at the top of the file. 
> This means that the strictness of typing for scalars is configured on a per-file basis. 
> This directive not only affects the type declarations of parameters, but also a function's return type.

The good thing about declaring a PHP file as strict is that it actually applies to **ONLY** the current file. 
It ensures that this file has strict types, but it doesn't apply to any other file in the whole project. 
It allows you to do, step by step, this migration from non-strict code to strict code, especially for new files or projects.

### Strict types affect coercion types

Using hint type without strict_types may lead to subtle bugs.
Prior to strict types, int $x meant $x must have a value coercible to an int. Any value that could be coerced to an int would pass the hint type, including:

- a proper `int` (example: 42 -> 42)
- a `float` (example: 13.1459 -> 13)
- a `bool` (example: `true` -> 1)
- a `null` (example: `null` -> 0)
- a `string` with leading digits (example: "15 Trees" -> 15)

By setting `strict_types=1`, you tell the engine that `int $x` means `$x must only be an int proper, no type coercion allowed`. 
You have the great assurance you're getting exactly and only what was given, without any conversion or potential loss.

### Who should care about this "strict type" line?

Actually, `declare(strict_types=1)` is more for the reader than for the writer. 
Why? Because it will explicitly tell the reader:
The types in this current scope (file/class) are treated strictly.

### 'strict_types=1' is more for the reader than for the writer

The writer just needs to maintain such strictness while writing the expected behavior. 
That said, as a writer, you should care about your readers, which also includes your future self. 
Because you are going to be one of them.

## References

* [Scalar type declarations](https://www.php.net/manual/en/migration70.new-features.php#migration70.new-features.scalar-type-declarations)
* [What do strict types do in PHP?](https://stackoverflow.com/q/48723637/3454593)
