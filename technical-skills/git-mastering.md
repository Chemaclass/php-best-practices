[Back to technical skills](../technical-skills)

# Git Mastering

> Using git via the terminal or via your IDE?

## Command Tool

It's true that you can use git with your IDE ([PhpStorm](./ide.md), for example) but you should know 
the fundamentals behind these "short-cuts" buttons.

Double check that you know exactly how the git commands work behind the scene using terminal
before you get use to these button-helpers.

```
git status
git checkout
git diff
git rebase
git pull
git push
git stash
git cherry-pick
...
```

You can even create your own aliases or use the ones that [omyzh](https://github.com/ohmyzsh/ohmyzsh/wiki/Cheatsheet#git) provide for you.

## Git Hooks

My favorite git hooks are:

- `pre-commit`: perfect to check the code style and run your unit tests. This one must be fast.
- `pre-push`: perfect to run your integration / functional / e2e tests.

This way, you will ensure that your "git commit" will have a minimum assert of quality, while
your "git push" will fully pass the CI.

Anyway, you can easily bypass any "git hook" using the `--no-verify` flag.
