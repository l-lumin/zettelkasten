# Reliable, Scalable, Maintainable Applications

An application has to meet various requirements in order to be useful. There are _functional requirements_ (what it should do, such as allowing data to be stored, retrieved, searched, and processed in various ways), and some _nonfunctional requirements_ (compliance, scalability, compatibility, and maintainability)

Three concerns important in most software systems

- Reliability: The system should continue to work correctly (performing the correct function at the desired level of performance) even in the face of adversity (hardware or software faults, and even human error)
- Scalability: As the system grows (in data volume, traffic volume, or complexity), there should be reasonable ways of dealing with that growth
- Maintainability: Over time, many different people will work on the system (engineering and operations, both maintaining current behavior and adapting the system to new use cases), and they should all be able to work on it productively

## Reliability

Reliability is continuing to work correctly, even when things go wrong
The things that can go wrong are called _faults_, and systems that anticipate faults and can cope with them are called _fault-tolerant_ or resilient
A fault is defined as one component of the system deviating from its spec, a failure is when the system as a whole stops providing the required service to the user.

### Types of Faults

- Hardware faults: Disk failure, memory errors,...
- Software faults:Bugs, memory leaks, unhandled exceptions,...
- Human errors
  Approaches prevent human errors:
- Design system that minimizes opportunities for error
- Decouple the places where people make the most mistake from the place where they can cause failures. Ex: sandbox
- Test
- Allow quick and easy recovery from human errors
- Set up detailed and clear monitoring (telemetry)
- Implement good management practices and training

## Scalability

Scalability means system's ability to cope with increased load

Describing load
Load can be described with a few numbers called _load parameters_. Ex: Post tweet, home timeline,...

Describing performance

Approaches for coping with load

- scaling up (vertical scaling): move to a more powerful machine
- Scaling out (horizontal scaling): distributing the load across multiple machines, also know as shared-nothing architecture
- Elastic: can automatically add and computing resources when detect aa load increase

## Maintainability

The majority of the cost of software is not its initial development, but in its ongoing maintenance.

Three design principles for software system:

- Operability: make it easy for operations team to keep the system run smoothly
- Simplicity: make it easy for new engineers to understand the system
- Evolvability: make it easy for engineers to make changes to the system in the future, adapting it for unanticipated use case as requirements change (known as extensibility, modifiability, plasticity)
