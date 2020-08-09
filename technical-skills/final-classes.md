[Back to technical skills](../technical-skills)

# Final classes

## Motivation

### Reduce the scope visibility to the minimum

When you see a class prefix with the `final` keyword you will be sure that this class is not extended by any other in the code, which makes it more readable.

### Help and encourage our "composition over inheritance" mentality

If there is any reason why we would like to leave a class non-final: remove the `final` keyword, or don't add it.

Any reason meaning: being aware we want to keep open a class to be extendable.

## Why is this class not final?

If we aim for composition over inheritance, then we should try to avoid inheritance as much as possible, and use it only when it's really necessary. Inheritance is often misused in OOP.

## Misconception

When we first taught OOP, we usually introduced the classic inheritance example.

Nonetheless, when [Alan Kay](http://lists.squeakfoundation.org/pipermail/squeak-dev/1998-October/017019.html) created Smalltalks, the inheritance is never the main concept of it. The main concept is messaging, which is you can send message to object and object encapsulate the data and logic in it, and we can change behavior by using different object, which actually is, composition. But the concept of inheritance is too popular that eventually overshadow composition. I think part of the reason is inheritance introduce an abstract layer from real world to explain object’s relation, which can make the code really easy to understand if we use it properly.

## Benefits

- Clear contracts; using interfaces will force you to think in the term of communication between objects.
- Isolated, side effect free code units; injecting interfaces only as dependencies will remove every nasty side effect around the code you are working on; changing an interface implementation won’t affect other concrete classes since they depend only on the interface abstraction.
- Testability; mocking dependencies is extremely easy when they are interfaces; no more “I forgot to disable the constructor / mock a concrete method” troubles in your System Under Test.
- Low, manageable complexity; as everything is isolated, you won’t need to worry about rippling changes; this dramatically decreases the complexity of your code.
- Low cognitive load; with decreased complexity, your brain will be free to focus on what matters.
- Code fluidity; removing any unnecessary coupling, you will be able to move things around way more easily than before.
- Confidence in yourself; being able to test your code in isolation so well will give you a wonderful sense of confidence in changing it.

## Composition over inheritance

- If you feel the need to reconfigure an object, to change parts of an algorithm, to rewrite part of the implementation, consider creating a new class instead of overriding an existing class.
- If you need to represent a hierarchy of classes, where subclasses are proper substitutes for their parent classes, this would be the classic situation where you may still consider inheritance. However, the result may still be better if you don't inherit from concrete parent classes but from abstract interfaces.

## What you should start doing instead

- use interfaces to define the contracts between your classes.
- use final classes to implement behavior for those interfaces.
- use composition (through constructor dependency injection) to put things together and prevent complexity.

## References

- [Final classes by default. Why?- Matthias Noback](https://matthiasnoback.nl/2018/09/final-classes-by-default-why/)
- [Inheritance is evil. Stop using it- Codeburst](https://codeburst.io/inheritance-is-evil-stop-using-it-6c4f1caf5117)
- [Why inheritance is bad- Neethack](http://neethack.com/2017/04/Why-inheritance-is-bad/)
- [When to declare classes final- Ocramius](https://ocramius.github.io/blog/when-to-declare-classes-final/)
- [Why is using final so bad?- Stackexchange](https://softwareengineering.stackexchange.com/questions/89073/why-is-using-final-on-a-class-really-so-bad)
- [Is inheritance a bad practice in OOP?- Quora](https://www.quora.com/Is-inheritance-bad-practice-in-OOP-Many-places-that-teach-design-patterns-say-to-opt-for-composition-over-inheritance-but-what-about-when-multiple-classes-share-logic-from-an-abstract-class-such-as-in-the-Template-Method-design-pattern)
