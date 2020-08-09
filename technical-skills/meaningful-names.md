[Back to technical skills](../technical-skills)

# Meaningful Names

The name of a variable, function, or class, should answer all the big questions. It should tell you why it exists, what it does, and how it is used. If a name requires a comment, then the name does not reveal its intent.

A variable's name represents what information it contains.

## Use intention revealing names
```php
// Bad
private $d; // elapsed time in days

// Good
private $elapsedTimeInDays;
```

## Use pronounceable names
```php
// Bad
class DtaRcrd102 
{
    /** @var Date */
    private  $genymdhms;

    /** @var Date */
    private $modymdhms;
}

// Good
class Customer 
{
    /** @var Date */
    private $generationTimestamp;

    /** @var Date */
    private $modificationTimestamp;
}
```
## Use searchable names

If a variable or constant might be seen or used in multiple places in a body of code, it is imperative to give it a search-friendly name.
```php
// Bad
for ($i = 0; $i < 34; $i++) {
    $s += ($t[$i] * 4) / 5;
}

// Good
const NUMBER_OF_TASKS = 34;
const WORK_DAYS_PER_WEEK = 5;
const REAL_DAYS_PER_IDEAL_DAY = 4;

$sum = 0;
for ($i = 0; $i < self::NUMBER_OF_TASKS; $i++) {
    $realTaskDays = $this->taskEstimate[$i] * self::REAL_DAYS_PER_IDEAL_DAY;
    $realTaskWeeks = $realTaskDays / self::WORK_DAYS_PER_WEEK;
    $sum += $realTaskWeeks;
}
```
Sum above is not really useful but at least is searchable. The intentionally named code makes the function longer, but check how easier it will be to find WORKS_DAYS_PER_WEEK than to find all the places where 5 was used.

## Class and Variables: always nouns

Classes and variables should have noun or noun phrase names like `Customer`, `WikiPage`, `Account`, and `AddressParser`.  

Avoid words like `Helper`, `Processor`, `Data`, or `Info` in the name of a class.

## Method Names

Methods should have verb or verb phrase names like `postPayment()`, `deletePage()`, or `save()`.

When constructors are overloaded, use static factory methods with names that describe the arguments.
```php 
// Bad
$fulcrumPoint = new Complex(23.0)

/// Good
$fulcrumPoint = Complex::fromRealNumber(23.0);
```

For methods/functions that return a boolean, must be predicated. 
For example: `isValid()` or `hasSomething()`.

## Pick one word per concept

When starting to have a huge code base, you and your team might start failing to be consistent in the concepts. That might end up having a `fetch`, `retrieve`, and `get` as equivalent methods of different classes.

We must use `find` in Repositories and `get` for Entities or Services.

## References

### Books

* **Clean Code** ([Amazon](https://www.amazon.de/-/en/dp/0132350882/)) [English] by Robert C. Martin

### Other links

* [Names++ - Clean Code, Episode 2](https://cleancoders.com/episode/clean-code-episode-2/show) 
