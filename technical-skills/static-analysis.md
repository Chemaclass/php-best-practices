# Static Analysis

If this is a completely new topic for you, I would recommend you to start with Psalm, for example. 
Their [documentation](https://psalm.dev/docs/) is simply amazing.

## Psalm

[Psalm](https://psalm.dev/) is an open-source static analysis tool for PHP that helps you identify both obvious and hard-to-spot bugs in your code.

Psalm is designed to be useful on both large legacy codebases and small, modern ones. It can help you prevent the vast majority of type-related runtime errors, and also enables you to take advantage of safe coding patterns popular in other languages.

Lastly, Psalm can automatically fix a number of the errors it finds, allowing you to improve your code without breaking a sweat.

## PHPStan

[PHPStan](https://phpstan.org/) focuses on finding errors in your code without actually running it. It catches whole classes of bugs even before you write tests for the code. 

It moves PHP closer to compiled languages in the sense that the correctness of each line of the code can be checked before you run the actual line.

## Phan

[Phan](https://github.com/phan/phan) is a static analyzer for PHP. Phan prefers to avoid false-positives and attempts to prove incorrectness rather than correctness.

## References

* [PHP static code analysis based on the example of PHPStan, Phan and Psalm](https://badootech.badoo.com/php-code-static-analysis-based-on-the-example-of-phpstan-phan-and-psalm-a20654c4011d)
