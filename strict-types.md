# Strict types

## Comparison

Don’t use loose comparison, always be as strict as possible.

```php
// Bad:
if ($a == $b) {/* ... */}

// Good:
if ($a === $b) {/* ... */}
```

## For null checks use comparison to null instead of invoking method is_null().

```php
// Bad:
if (is_null($variable)) {/* ... */}

// Good:
if (null === $variable) {/* ... */}

// Also good:
if (!$variable) {/* ... */}
```

## Use strict_types constant when possible

We should specify the parameters types and even specify the return value (even `void` for nonreturn value).

We should write at the top of each PHP file

```php
<?php declare(strict_types=1);
// ...
```

By doing this, we will force our PHP code to be more correct and self-documenting. By default, scalar type-declarations are non-strict, which means they will attempt to change the original type to match the type specified by the type-declaration.

We must write, whenever is possible, the types for every parameter and returning value per function/method. Therefore, we should avoid writing unnecessary PHPDoc which duplicate the information already given by the real code.


#### Bad example
```php
/**
 * @var string $foo 
 * @var int $bar
 * @return void
 */
public function doSomeAction($foo, $bar)
{
    // ...
}
```

#### Good example
```php
// NOTICE: No PHPDoc is really necesary because the code is already self-documented
public function doSomeAction(string $foo, int $bar): void
{
    // ...
}
```

### Disclaimer

Adding `declare(strict_types=1)` for existing files should be avoided unless they are thoroughly tested. It's because we might receive numbers as strings (or viceversa) from external sources (REST APIs).

These are properly working cases as of today and unless you explicitly cast them to their primitive type it can cause future Fatal Errors. 
