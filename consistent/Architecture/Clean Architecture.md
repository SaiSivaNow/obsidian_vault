The goal of software architecture is to minimize the human resources required to build and maintain the required system.

**Use Cases (Adding/Supporting UseCases should be optimized) ?**

There are very few behavioral options that the architecture can leave open. But influence isn’t everything. The most important thing a good architecture can do to support behavior is to clarify and expose that behavior so that the intent of the system is visible at the architectural level.

**Opearation (Throughput of the system should be optimized) ?**

Meeting the needs of operation would require running it efficiently in vertically scaled processes, multiple threads, multiple processes, or multiple services. Or we can solve it by simply throwing more hardware.

Answer : By comparison, an architecture that maintains the proper isolation of its components, and does not assume the means of communication between those components, will be much easier to transition through the spectrum of threads,processes, and services as the operational needs of the system change over time. 

Almost any operational difficulty can be resolved by throwing more hardware at the system without drastically impacting the software architecture. Indeed, we have seen this happen over and over again. Software systems that have inefficient architectures can often be made to work effectively simply by adding more storage and more servers. The fact that hardware is cheap and people are expensive means that architectures that impede operation are not as costly as architectures that impede development, deployment, and maintenance

Perhaps a better way to say this is that the architecture of a system makes the operation of the system readily apparent to the developers. Architecture should reveal operation.The architecture of the system should elevate the use cases, the features, and the required behaviors of the system to first-class entities that are visible landmarks for the developers. This simplifies the understanding of the system and, therefore, greatly aids in development and maintenance.

The point being made here is that sometimes we have to separate our
components all the way to the service level. To take advantage of the operational benefit, the decoupling must have the appropriate mode. To run in separate servers, the separated components cannot depend on being together in the same address space of a processor. They must be independent services, which communicate over a network of some kind.

**Devolpment (Development done by different should be easy and independent)**

On the other hand, a system being developed by five different teams, each of
which includes seven developers, cannot make progress unless the system is divided into well-defined components with reliably stable interfaces. If no other factors are considered, the architecture of that system will likely evolve into five components—one for each team. Such a component-per-team architecture is not likely to be the best architecture for deployment, operation, and maintenance of the system. Nevertheless, it is the architecture that a group of teams will gravitate toward if they are driven solely by development schedule.

A system that must be developed by an organization with many teams and many concerns must have an architecture that facilitates independent actions by those teams,so that the teams do not interfere with each other during development. This is accomplished by properly partitioning the system into well-isolated, independently
developable components. Those components can then be allocated to teams that can work independently of each other.

Decoupling for developbility
1. If UI layer is decoupled from Business Rules. Then one can not impact each other.
2. If addOrder usecase is decoupled from deleteOrder usecase then two teams can work on them independenly withour interfering with each other.

 (layers and use cases are decoupled) --> (feature teams, component teams, layer teams or some other variation)


**Deployment (Deploying a new feature/usecase/bug should be easy and optimized)**

To be effective, a software system must be deployable. The higher the cost of deployment, the less useful the system is. A goal of a software architecture, then, should be to make a system that can be easily deployed with a single action.

The architecture also plays a huge role in determining the ease with which the system is deployed. The goal is “immediate deployment.” A good architecture does not rely on dozens of little configuration scripts and property file tweaks. It does not require manual creation of directories or files that must be arranged just so. A good architecture helps the system to be immediately deployable after build. Again, this is achieved through the proper partitioning and isolation of the components of the system, including those master components that tie the whole system together and
ensure that each component is properly started, integrated, and supervised.

The decoupling of the use cases and layers also affords a high degree of flexibility in deployment. Indeed, if the decoupling is done well, then it should be possible to hot-swap layers and use cases in running systems. Adding a new use case could be a simple as adding a few new jar files or services to the system while leaving the rest alone.

**Maintainance (Fixing bugs and adding a new case should be easy)**

Of all the aspects of a software system, maintenance is the most costly. The never-ending parade of new features and the inevitable trail of defects and corrections consume vast amounts of human resources. The primary cost of maintenance is in spelunking and risk. Spelunking is the cost of digging through the existing software, trying to determine the best place and the best strategy to add a new feature or to repair a defect. While making such changes, the likelihood of creating inadvertent defects is always there, adding to the cost of risk. A carefully thought-through architecture vastly mitigates these costs. By separating the system into components, and isolating those components through stable interfaces, it is possible to illuminate the pathways for future features and greatly reduce the risk of inadvertent breakage

Solution for optimizing about values of Software

The goal of the architect is to create a shape for the system that recognizes policy as the most essential element of the system while making the details irrelevant to that policy. This allows decisions about those details to be delayed and deferred.

A good architecture balances all of these concerns with a component structure that mutually satisfies them all. 

The reality is that achieving this balance is pretty hard. The problem is that most of the time we don’t know what all the use cases are, nor do we know the operational constraints, the team structure, or the deployment requirements. Worse, even if we did
know them, they will inevitably change as the system moves through its life cycle. In short, the goals we must meet are indistinct and inconstant. Welcome to the real world

Some principles of architecture are relatively inexpensive to
implement and can help balance those concerns, even when you don’t have a clear picture of the targets you have to hit. Those principles help us partition our systems into well-isolated components that allow us to leave as many options open as possible, for as long as possible.A good architecture makes the system easy to change, in all the ways that it must change,by leaving options open.


Solution : 
Decoupling Layers.
1. UI
2. Business Rules.
3. Application Rules.
4. Database Layer.