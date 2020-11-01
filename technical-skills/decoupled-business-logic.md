[Back to technical skills](../technical-skills)

# Decoupled business logic

> Abstraction, concretions, layers, and dependencies.

## Your business logic should be decoupled

Don't couple your business domain logic with any infrastructure code. 

**Infrastructure code is everything that has nothing to do directly with the logic of your business**. What is NOT business logic?

- the framework that you are using
- the connection to the database
- the I/O system
 
All of these are irrelevant details that should not be attached to your business logic.

> In order to accomplish this goal, we should depend on abstractions (interfaces) instead of concretions.

## A complete application consists of three major layers

- Domain
- Application
- Infrastructure

### The (business) domain layer

The domain layer contains the domain entities and stand-alone domain services. 
Any domain concepts (this includes domain services, but also repositories) that depend on external resources, are defined by **interfaces**.

### The application layer

The application layer contains the implementation of the application services. 
These services shouldn't have "business logic" in them, even though they orchestrate the steps required to fulfill the commands imposed by the client.
The main difference between the domain and the application services is that domain services hold domain logic whereas application services don’t.

### The infrastructure layer 

The infrastructure layer **contains the implementation of the interfaces from the domain layer**. 
These implementations may introduce new non-domain dependencies that have to be provided to the application. 
Usually, the infrastructure layer is where all non-relevant-to-your-domain-details are placed.

## Benefits

- Easy **testability**. When your business logic depend on abstractions (interfaces) you can easily create unit tests for all possible combinations of its behavior.
- Your business logic became **easy to be replaced** and to be adapted to the new requirements.
- **Loosely couple** with infrastructure code. When your logic depends on abstraction, you can postpone the details to the end and rather focus on the business requirements. 

## References

- [Advanced Web Application Architecture | Matthias Noback](https://leanpub.com/web-application-architecture/)
