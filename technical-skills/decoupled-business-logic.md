[Back to technical skills](../technical-skills)

# Decoupled business logic

> Abstraction, concretions, layers and dependencies.

## A complete application consists of three major layers

- Domain
- Infrastructure
- Application

### The domain layer

The domain layer contains the domain entities and stand-alone domain services. 
Any domain concepts (this includes domain services, but also repositories) that depend on external resources, are defined by *interfaces*.

### The infrastructure layer 

The infrastructure layer *contains the implementation of the interfaces from the domain layer*. 
These implementations may introduce new non-domain dependencies that have to be provided the application. 
These are the application services and are represented by interfaces.

### The application layer

The application layer contains the implementation of the application services. 
These services shouldn't have "business logic" in them, even though they orchestrate the steps required to fulfill the commands imposed by the client.
Typically, these will make calls to the infrastructure services, domain services, and Domain Entities in order to get the job done.

#### What's the main difference between domain services and application services?

The main difference between them is that domain services hold domain logic whereas application services don’t.

## References

- [Stackoverflow](https://stackoverflow.com/questions/2268699/domain-driven-design-domain-service-application-service/5252647#5252647)
- [Bennadel's blog](https://www.bennadel.com/blog/2385-application-services-vs-infrastructure-services-vs-domain-services.htm)
