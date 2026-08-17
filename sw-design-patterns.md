### Software Desing Patterns

Based on article on wiki's article [Software Design Patterns](https://en.wikipedia.org/wiki/Software_design_pattern)

- `DP` - Design Patterns. Elements of Reusable Object-Oriented Software
- `CC` - Code Complete by Steve McConnell
- `EA` - PoEAA or Patterns of Enterprise Application Architecture
- `3D` - Domain-Driven Design (DDD)
- `??` - somewhere else...
- `--` - not specified...

#### Creational
- `DP``CC``--`👌Abstract Factory. It’s OK.
- `DP``CC``--`🚫Builder. Terrible concept, since it encourages us to create and use big, complex objects. If you need a builder, there is already something wrong in your code. Refactor it so any object is easy to create through its constructors.
- `CC``--``--` Dependency Injection. A class accepts the objects it requires from an injector instead of creating the objects directly.
- `DP``CC``--`🚫Factory Method. This one seems OK. It’s bad!
- `DP``CC``EA`👌Lazy Initialization. It’s OK.
- `DP``CC``??`🚫Multiton. Really bad idea. Same as Singleton.
- `DP``CC``??`✅Object Pool. Good one.
- `DP``CC``??`✅Prototype. Good idea, but what does it have to do with OOP?
- `DP``CC``??`✅RAII. Resource acquisition is initialization. This is a really good one, and I highly recommend you use it.
- `DP``CC``??`🚫Singleton. It’s the king of all anti-patterns. Stay away from it at all costs.

#### Structural
- `DP``CC``??`✅Adapter. Good one!
- `DP``CC``??`✅Bridge. Good one!
- `DP``CC``??`✅Composite. Good one; check out this too.
- `DP``CC``??`✅Decorator. My favorite one. I highly recommend you use it.
- `DP``CC``??`Delegation. Extend a class by composition instead of subclassing. The object handles a request by delegating to a second object (the delegate).
- `DP``CC``??`Extension object. Adding functionality to a hierarchy without changing the hierarchy.
- `DP``CC``??`🚫Facade. Bad idea. In OOP, we need objects and only objects, not facades for them. This design pattern is very procedural in its spirit, since a facade is nothing more than a collection of procedures.
- `DP``CC``??`🚫Flyweight. It’s a workaround, as I see it, so it’s not a good design pattern. I would recommend you not use it unless there is a really critical performance issue. But calling it a design pattern … no way. A fix for a performance problem in Java? Yes.
- `DP``CC``??`🚫Front Controller. Terrible idea, as well as the entire MVC. It’s very procedural, that’s why.
- `DP``CC``??`✅Proxy. Good one.
- `DP``CC``??`Twin. Twin allows modeling of multiple inheritance in programming languages that do not support this feature.

#### Behavioral
- `DP``CC``??`Blackboard. ..
- `DP``CC``??`👌Chain of Responsibility. Seems fine.
- `DP``CC``??`👌Command. It’s OK.
- `DP``CC``??`Fluent interface. ..
- `DP``CC``??`👌Interpreter. It’s OK, but I don’t like the name. “Expression” would be a much better alternative.
- `DP``CC``??`🚫Iterator. Bad idea, since it is mutable. It would be much better to have immutable “cursors.”
- `DP``CC``??`🚫Mediator. I don’t like it. Even though it sounds like a technique for decreasing complexity and coupling, it is not really object-oriented. Who is this mediator? Just a “channel” between objects? Why shouldn’t objects communicate directly? Because they are too complex? Make them smaller and simpler, rather than inventing these mediators.
- `DP``CC``??`🚫Memento. This idea implies that objects are mutable, which I’m against in general.
- `DP``CC``??`✅Null Object. Good one. By the way, see Why NULL Is Bad
- `DP``CC``??`👌Observer. or Publish-Subscribe. The idea is good, but the name is bad, since it ends with -ER. A much better one would be “Source” and “Target.” The Source generates events and the Target listens to them.
- `DP``CC``??`🚫Servant. A very bad idea, because it’s highly procedural.
- `DP``CC``??`✅Strategy. A good one.
- `DP``CC``??`🚫Template Method. is wrong, since implementation inheritance is procedural.
- `DP``CC``??`🚫Visitor. A rather procedural concept that treats objects as data structures, which we can manipulate.
- `3D`👌State. Although it’s not implied, I feel that in most cases the use of this pattern results in mutability, a code characteristic that I’m generally against.

#### Architectural
- 🚫Data Transfer Object. It’s just a shame.
- 🚫MVC. Bad idea, since it’s very procedural. Controllers are the key broken element in this concept. We need real objects, not procedural controllers.
- 🚫ORM. It’s terrible and “offensive”; check this out.
- 👌Specification. It’s OK.

### others
- 🚫[Marker](https://en.wikipedia.org/wiki/Marker_interface_pattern). It’s a terrible idea, along with reflection and type casting.
- 🚫[Module](https://en.wikipedia.org/wiki/Module_pattern). If Wikipedia is right about this pattern, it’s something even more terrible than the Singleton.

<div align="right">
  <a href="#software-desing-patterns" alt="up &#8593;">up &#8593;</a>
</div>

---
### List
- Gang of Four patterns	
	- [Creational](#creational)
		- Abstract factory
		- Builder
		- Factory method
		- Prototype
		- Singleton
	- [Structural](#structural)
		- Adapter
		- Bridge
		- Composite
		- Decorator
		- Facade
		- Flyweight
		- Proxy
	- [Behavioral](#behavioral)
		- Chain of responsibility
		- Command
		- Interpreter
		- Iterator
		- Mediator
		- Memento
		- Observer
		- State
		- Strategy
		- Template method
		- Visitor
- Concurrency patterns	
	- Active object
	- Balking
	- Binding properties
	- Double-checked locking
	- Event-based asynchronous
	- Guarded suspension
	- Join
	- Lock
	- Monitor
	- Proactor
	- Reactor
	- Read–write lock
	- Scheduler
	- Scheduled-task pattern
	- Semaphore
	- Thread pool
	- Thread-local storage
- [Architectural patterns](#architectural)	
	- Front controller
	- Interceptor
	- MVC (MVP, MVVM)
	- MVI
	- ADR
	- ECS
	- Multitier architecture
	- vertical
	- hexagonal
	- Specification
	- Publish–subscribe
	- Naked objects
	- Service locator
	- Active record
	- Identity map
	- Data access object (DAO)
	- Data transfer object (DTO)
	- Inversion of control
	- Model
	- 2Broker
- Other patterns	
	- Blackboard
	- Business delegate
	- Composite entity
	- Composition over inheritance
	- Dependency injection
	- Guard clause
	- Intercepting filter
	- Lazy loading
	- Mock object
	- Null object
	- Object pool
	- Servant
	- Twin
	- Type tunnel
	- Method chaining
	- Delegation
- Books
	- [Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns)
	- [Enterprise Integration Patterns](https://en.wikipedia.org/wiki/Enterprise_Integration_Patterns)
- [Anti-pattern](https://en.wikipedia.org/wiki/Anti-pattern)
	- Software engineering, e.g.:
		- God object
		- Magic number
		- Poltergeist
		- Big Ball of Mud
	- Project management, e.g.:
		- Blowhard Jamboree. An excess of industry pundits
		- [Analysis paralysis](https://en.wikipedia.org/wiki/Analysis_paralysis)
		- Viewgraph Engineering. Too much time spent making presentations and not enough on the actual software.
		- Death by Planning. Spending too much effort planning.
		- Fear of Success. Irrational fears near to project completion.
		- The Corncob. Difficulties with people.[vague]
		- Intellectual Violence. Intimidation through use of jargon or arcane technology
		- Irrational Management. Bad management habits.
		- [Smoke and Mirrors](https://en.wikipedia.org/wiki/Smoke_and_mirrors). Excessive use of demos and prototypes by salespeople.
		- Throw It Over the Wall. Forcing fad software engineering practices onto developers without buy-in.
		- Fire Drill. Long periods of monotony punctuated by short crises.
		- The Feud. Conflicts between managers.
		- e-mail Is Dangerous. Situations resulting from ill-advised e-mail messages.
- [Architectural pattern](https://en.wikipedia.org/wiki/Software_architecture#Pattern)
	- Software architecture pattern, e.g.:
		- Circuit Breaker
	- Software architecture style, e.g.:
		- Layered
		- Microservices
		- Event-Driven

[up &#8593;](#software-desing-patterns)
