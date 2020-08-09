[Back to team work](../team-work)

# Code Reviews

## Benefits

* It helps to share the changes (and therefore knowledge) with the rest of your colleagues.
* It helps to double-check if the changes are the correct ones or you might have forgotten something important while doing your changes.

## Common approaches

* Pair Programming
* By creating a Pull Request

### Pair Programming

Pairing is the act of two people working together on a single programming problem.

Pairing programmers sometimes adopt different roles. One may be the driver and the other the navigator.

Most often, however, there are no roles at all. The programmers are simply co-equal authors sharing the mouse and keyboard in a cooperative manner.

Pairs are not scheduled. They are generally short-lived. They are often not more than an hour or two.

Pair Programing shouldn't be just for Seniors to mentor Juniors. 

It shouldn't be mandatory but highly recommended due it's benefits:

* The members of a team do not work in isolation from each other.
* Is the best way, by far, to share knowledge between team members and prevent knowledge silos from forming.
* It's the best way to make sure that nobody on the team is indispensable.

While you practice Pair Programming the code it's being reviewed all the time. Two brains think better than one.
Thus, the review is not simply a static check to ensure that the team's coding standards are applied. 
Rather, it's a dynamic review of the current state of the code with an eye to where the code needs to be in the near future.


### Pull Request (PR)

#### Your checklist for a pull request

* You should cover all new functionality with tests
* You should ensure that all functionality that you touched or modified somehow are covered by tests
* All the tests must be green

#### Mandatory description

The purpose of the PR description is to eliminate the dependency on external resources for completing a PR. 
External tickets (from Jira, for example) might only contain WHAT has to be done (aka: Acceptance Criteria), 
and may or may not contain technical details needed to understand the PR.

Recommendations for a great PR description message:

1. Include Information about what the PR is about
1. Point to the PR's entry point (if applicable)
1. Describe why you pick up that solution (if you already tried other ones or it just makes sense to mention them)
1. Guide with technical inputs related to the PR
1. In the case of refactoring, justify it
1. Screenshots for frontend PRs

The PR description should be like the conversation between the author and the reviewer. 
Is the context that the reviewer will read just before start reading the code. 
It will provide some background that will facilitate the required understanding to do the review process 
smoother and easier for the reviewer.

Tricks that might help you to put on the shoes of your reviewer colleagues:

As a non-author dev:

* What would I like to know before starting reading the code?
* Where should I start reading the code? Where is the entry point in this N files changes?
* Why the author pick this technical solution if there are another N possible solutions?
* Might a picture/screenshot help to clarify some ideas?

## References

### Books

* **Extreme Programming Explained: Embrace Change** ([Amazon](https://www.amazon.de/-/en/dp/B00N1ZN6C0/)) [English] by Kent Beck, Cynthia Andres
* **Clean Agile** ([Amazon](https://www.amazon.de/-/en/dp/B07XTL99JQ/)) [English] by Robert C. Martin

