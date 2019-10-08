# Strict types

Being aware that we are using one of the latest PHP version (7.2), we should also know the potential that it brings to us. We can specify the parameters types and even specify the return value (even `void` for nonreturn value).

We SHOULD write at the top of each PHP file

```php
<?php

declare(strict_types=1);
```

By doing this, we will force our PHP classes to be more correct and self-documenting. By default, scalar type-declarations are non-strict, which means they will attempt to change the original type to match the type specified by the type-declaration.

We MUST write, whenever is possible, the types for every parameter and returning value per function. Therefore, we should avoid writing unnecessary PHPDoc which duplicate the information already given by the real code.


### Bad
```php
/**
 * @var string $foo 
 * @var int $bar
 *
 * @return void
 */
public function doSomeAction($foo, $bar)
{
    // ...
}
```

### Good
```php
// NOTICE: No PHPDoc is really necesary because the code is already self-documented
public function doSomeAction(string $foo, int $bar): void
{
    // ...
}
```

## Disclaimer

Adding `declare(strict_types=1)` for existing files should be avoided unless they are thoroughly tested. It's because we often receive numbers as strings from external sources (AfterShip/Tracker, REST APIs).
These are properly working cases as of today and unless you explicitly cast them to their primitive type it can cause future Fatal Errors. 