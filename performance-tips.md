# Performance tips

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

