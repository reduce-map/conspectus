# Base Patterns

## 1. GRASP Patterns (General Responsibility Assignment Software Patterns)

- **Information Expert:** Responsibility is assigned to the class that has the necessary information to fulfill it.
- **Creator:** The class that aggregates or manages other objects is responsible for creating them.
- **Controller:** Acts as an intermediary between the user and the system, handling requests and coordinating actions of other objects.
- **Low Coupling:** Reduces dependencies between classes to facilitate changes and increase code resilience.
- **High Cohesion:** Each class should be focused on a single task, making the system easier to understand and maintain.
- **Polymorphism:** Uses a common interface to handle alternative behaviors based on the object's type.
- **Pure Fabrication:** Creates a helper class that is not part of the domain but solves a specific architectural problem.
- **Indirection:** Introduces an intermediate object to reduce the coupling between other objects.
- **Protected Variations:** Identifies potential points of change in the system and protects them through the use of abstractions.

## 2. Design Patterns Gang of Four (GoF)

### Creational Patterns

- **Factory Method:** Defines an interface for creating an object but lets subclasses alter the type of objects that will be created.
- **Abstract Factory:** Provides an interface for creating families of related or dependent objects without specifying their concrete classes.
- **Builder:** Separates the construction of a complex object from its representation, allowing the same construction process to create different representations.
- **Prototype:** Specifies the kinds of objects to create using a prototypical instance, and creates new objects by copying this prototype.
- **Singleton:** Ensures a class has only one instance and provides a global point of access to it.
- **Object Pool:** Manages a pool of reusable objects, allowing for the reuse of costly resources and limiting the number of instances created.

### Structural Patterns

- **Adapter:** Converts the interface of a class into another interface the clients expect. Adapter lets classes work together that couldn't otherwise because of incompatible interfaces.
- **Decorator:** Attaches additional responsibilities to an object dynamically. Decorators provide a flexible alternative to subclassing for extending functionality.
- **Composite:** Composes objects into tree structures to represent part-whole hierarchies. Composite lets clients treat individual objects and compositions of objects uniformly.
- **Bridge:** Decouples an abstraction from its implementation so that the two can vary independently.
- **Flyweight:** Uses sharing to support large numbers of fine-grained objects efficiently.
- **Facade:** Provides a unified interface to a set of interfaces in a subsystem. Facade defines a higher-level interface that makes the subsystem easier to use.

### Behavioral Patterns

- **Chain of Responsibility:** Passes a request along a chain of handlers. Upon receiving a request, each handler either processes the request or passes it to the next handler in the chain.
- **Command:** Encapsulates a request as an object, thereby letting you parameterize clients with queues, requests, and operations.
- **Interpreter:** Given a language, defines a representation for its grammar along with an interpreter that uses the representation to interpret sentences in the language.
- **Iterator:** Provides a way to access the elements of an aggregate object sequentially without exposing its underlying representation.
- **Mediator:** Defines an object that encapsulates how a set of objects interact. Mediator promotes loose coupling by keeping objects from referring to each other explicitly.
- **Memento:** Without violating encapsulation, captures and externalizes an object's internal state so that the object can be restored to this state later.
- **Observer:** Defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.
- **State:** Allows an object to alter its behavior when its internal state changes. The object will appear to change its class.
- **Strategy:** Defines a family of algorithms, encapsulates each one, and makes them interchangeable.
- **Template Method:** Defines the skeleton of an algorithm in a method, deferring some steps to subclasses.
- **Visitor:** Represents an operation to be performed on the elements of an object structure. Visitor lets you define a new operation without changing the classes of the elements on which it operates.

## 3. Enterprise Integration Patterns

- **Message Channel:** Establishes a channel for communication between systems, allowing messages to be exchanged.
- **Message Endpoint:** Defines an interface for sending and receiving messages within an enterprise system.
- **Message Router:** Directs messages to different channels based on specific conditions or content of the message.
- **Message Translator:** Converts a message from one format to another to ensure compatibility between different systems.
- **Message Broker:** Acts as an intermediary that routes, transforms, and processes messages between systems.
- **Message Filter:** Filters messages based on certain criteria before allowing them to pass to the next stage.
- **Aggregator:** Collects related messages and combines them into a single message before processing.
- **Splitter:** Breaks a single message into multiple smaller messages for separate processing.
- **Content Enricher:** Adds additional data to a message to enhance its information content before processing.

## 4. Architecture Patterns

- **Layered Architecture:** Divides the system into layers with distinct responsibilities (e.g., presentation, business logic, data access) to enhance modularity and maintainability.
- **Microservices Architecture:** Structures the application as a collection of small, autonomous services that communicate over a network.
- **Event-Driven Architecture:** Uses events as the central mechanism for communication between services or components, promoting loose coupling.
- **Service-Oriented Architecture (SOA):** Organizes the system into services that provide reusable functionality, accessible over a network.
- **Monolithic Architecture:** Combines all the functionalities of an application into a single, unified codebase and deployable unit.
- **Client-Server Architecture:** Splits the system into client and server components, where clients request services and servers provide them.
- **MVC (Model-View-Controller):** Separates application logic, user interface, and input control into three interconnected components to improve modularity and flexibility.
- **Hexagonal Architecture (Ports and Adapters):** Isolates the core logic of the system from external systems and technologies, making it easier to change or replace them.

## 5. Concurrency Patterns

- **Thread Pool:** Manages a pool of worker threads that can be reused to perform tasks, reducing the overhead of thread creation and management.
- **Locking:** Provides mechanisms to ensure that only one thread can access certain resources at a time, preventing race conditions.
- **Monitor Object:** Synchronizes access to an object so that only one thread can execute its critical section at a time.
- **Active Object:** Decouples method execution from method invocation to enhance concurrent execution and control over synchronization.
- **Fork/Join:** Breaks a task into smaller subtasks that can be executed concurrently, and then combines their results.
- **Scheduler:** Manages the execution of tasks by scheduling them to run at certain times or in response to specific events.
- **Producer-Consumer:** Synchronizes the work of producer threads, which generate data, and consumer threads, which process that data, using a shared buffer.
- **Immutable Object:** Designates objects whose state cannot be modified after creation, ensuring thread safety without synchronization.

## 6. Reactive Patterns

- **Observer:** Establishes a subscription mechanism to allow objects to be notified automatically when the state of another object changes.
- **Event Sourcing:** Captures all changes to the application's state as a sequence of events, which can be replayed to restore or analyze state.
- **Backpressure:** Manages the flow of data between components to prevent overwhelming slower components with too much data at once.
- **Circuit Breaker:** Monitors the interactions between services and temporarily halts them to prevent cascading failures when one service becomes unresponsive.
- **Publisher-Subscriber:** Allows multiple subscribers to listen to events from a publisher without the publisher needing to know the subscribers.
- **Reactive Streams:** Specifies a standard for asynchronous stream processing with non-blocking backpressure.
- **Message Passing:** Facilitates communication between components or services by sending messages rather than invoking methods directly.
- **Asynchronous Messaging:** Decouples the sending and receiving of messages in time, allowing for more flexible and resilient communication.

## 7. Security Patterns

- **Authentication:** Ensures that the system correctly identifies users or systems before allowing access.
- **Authorization:** Manages permissions, ensuring that users can only perform actions they are allowed to.
- **Access Control List (ACL):** Defines which users or system processes are granted access to objects and what operations are allowed.
- **Secure Session Management:** Maintains and secures user sessions, ensuring that session data is not intercepted or hijacked.
- **Encryption:** Protects data by transforming it into a secure format that can only be read by authorized parties.
- **Intrusion Detection System (IDS):** Monitors and analyzes system activities to detect and alert on potential security breaches.
- **Firewall:** Controls the flow of network traffic based on predetermined security rules, protecting the system from unauthorized access.
- **Security Token:** Represents a user’s credentials or other sensitive information in a secure, verifiable format that can be used to authenticate and authorize access.
- **Single Sign-On (SSO):** Allows users to authenticate once and gain access to multiple related systems without being prompted to log in again.
- **Audit Trail:** Keeps a record of system activities and accesses to provide accountability and traceability of actions taken within the system.

## 8. Distributed Systems Patterns

- **Leader Election:** Ensures that one node in a distributed system is chosen as the leader to coordinate tasks and manage resources.
- **Replication:** Duplicates data or services across multiple nodes to ensure availability and fault tolerance.
- **Sharding:** Splits data across multiple databases or nodes to improve performance and manageability.
- **Consensus:** Ensures that all nodes in a distributed system agree on a certain state or value, typically used in distributed databases or blockchain technology.
- **Quorum:** Requires a majority of nodes to agree on a decision before it is finalized, increasing the consistency and reliability of operations.
- **Data Consistency:** Ensures that data remains consistent across distributed nodes, even in the presence of failures or concurrent updates.
- **Eventual Consistency:** Allows for temporary inconsistencies in data across nodes, with the guarantee that all nodes will eventually converge to the same state.
- **Distributed Transactions:** Manages transactions across multiple nodes, ensuring atomicity and consistency in distributed environments.
- **Service Discovery:** Enables dynamic discovery of services in a distributed system, allowing nodes to find and connect with each other without prior knowledge.

## 9. Microservices Patterns

- **Service Registry:** A centralized directory where all microservices register themselves upon startup and where clients can discover and connect to available services dynamically.
- **API Gateway:** A single entry point for all client requests to microservices. It handles tasks such as request routing, load balancing, authentication, rate limiting, and monitoring. It can also provide a unified interface to various microservices.
- **Circuit Breaker:** Protects microservices from cascading failures by detecting when a service is likely to fail and temporarily halting requests to that service until it recovers.
- **Saga:** Manages distributed transactions in a microservices architecture by coordinating a series of local transactions. If a step fails, the Saga will execute compensating transactions to undo the work that was completed by previous steps.
- **CQRS (Command Query Responsibility Segregation):** Separates the methods for reading and writing data. This pattern allows for optimized read and write operations, as well as scalability improvements, particularly useful in systems where read and write operations have very different performance requirements.
- **Service Mesh:** An infrastructure layer for handling service-to-service communication. It provides features like load balancing, service discovery, traffic management, and security (e.g., mutual TLS), abstracting these concerns away from the business logic.
- **Sidecar:** A companion service that runs alongside a primary service within the same deployment unit (e.g., a Docker container). The sidecar often handles infrastructure concerns such as logging, monitoring, or proxying requests, allowing the primary service to focus solely on business logic.
- **Health Check:** Regularly monitors the health of microservices to ensure they are functioning correctly. If a service is unhealthy, it can be restarted or its traffic can be rerouted to a healthy instance.
- **Distributed Tracing:** Tracks requests as they propagate through multiple microservices, providing visibility into the flow and performance of requests, and helping to diagnose latency issues or failures.
- **Bulkhead:** Isolates different parts of a system to prevent a failure in one part from cascading to others. Each service is compartmentalized, so that if one fails, others can continue functioning.
- **Backends for Frontends (BFF):** Creates a unique API gateway or backend service for each client type (e.g., web, mobile). This pattern helps tailor the backend services to the needs of different frontends, improving performance and user experience.
- **Event Sourcing:** Stores the state of a system as a sequence of events. Instead of saving the current state, each change is captured as an event, allowing the system to rebuild the state by replaying these events. This is particularly useful in microservices for ensuring consistency across services.
- **Command and Event-Driven Communication:** Uses commands to initiate a process and events to notify other services of changes or completion. This pattern supports asynchronous processing and decouples services, improving scalability and reliability.
- **Database per Service:** Ensures each microservice manages its own database. This pattern enforces strong encapsulation and independence, allowing services to be deployed, scaled, and managed independently.
- **Strangler Fig:** Gradually replaces parts of a monolithic system with microservices. The existing monolithic application is refactored and new functionality is built as microservices, eventually "strangling" the old system until it can be fully replaced.
- **Decomposition by Subdomain:** Breaks down a system into microservices based on the bounded contexts or subdomains defined in domain-driven design (DDD). Each microservice is responsible for a specific business capability.
- **Externalized Configuration:** Stores configuration settings outside the application code, often in a centralized configuration service. This allows for easy updates and consistency across microservices, especially during deployment and scaling.
- **Blue-Green Deployment:** Deploys a new version of a service alongside the old one, allowing for quick rollback if issues arise. The "blue" environment is the current live system, while the "green" environment is the new version being tested.
- **Canary Release:** Gradually rolls out a new version of a microservice to a small subset of users before full deployment. This approach helps catch potential issues early without affecting all users.
- **Shadowing (Testing in Production):** Duplicates live traffic and sends it to a new version of a microservice running in parallel, allowing for real-world testing without affecting production users.
- **Service Choreography:** Decentralizes coordination among microservices, allowing each service to decide how to respond to events and interact with other services. This pattern contrasts with orchestration, where a central service manages the workflow.
- **Versioned API:** Maintains multiple versions of an API to ensure backward compatibility as new features are added or changes are made. Clients can choose which version of the API to use, ensuring stability for existing consumers while allowing for innovation.
- **Timeouts and Retries:** Defines time limits for requests between microservices and automatically retries failed requests. This helps improve system resilience by handling transient failures gracefully.
- **Idempotency:** Ensures that repeated execution of a request has the same effect as a single execution, which is crucial in distributed systems where network issues can lead to duplicate requests.
- **Remote Procedure Call (RPC):** Enables microservices to communicate with each other by calling functions over a network as if they were local. This pattern can simplify interactions but may introduce tight coupling between services.
- **API Composition:** Combines multiple microservices' responses into a single output. This pattern is often implemented by an API gateway or aggregator service to optimize client interactions.
- **Eventual Consistency:** Allows microservices to have temporarily inconsistent states, with the guarantee that they will eventually converge to the same state. This pattern is essential in distributed systems where immediate consistency is challenging to achieve.
- **Rate Limiting:** Controls the number of requests a service can handle within a certain timeframe. This protects services from being overwhelmed by too many requests, especially in public APIs.
- **Token-Based Authentication:** Uses tokens to authenticate and authorize requests between clients and microservices. Tokens can include user credentials, roles, or other claims and are typically issued by an identity provider.
- **Cross-Origin Resource Sharing (CORS):** Manages how web applications interact with resources hosted on different domains, ensuring secure and controlled access to APIs from different origins.

## 10. Cloud Design Patterns

- **Auto-Scaling:** Automatically adjusts the number of resources based on current demand to optimize performance and cost.
- **Load Balancer:** Distributes incoming network traffic across multiple servers to ensure no single server becomes a bottleneck.
- **Circuit Breaker:** Prevents a network service from repeatedly failing by breaking the connection if too many requests fail in a short period.
- **Throttling:** Limits the number of requests or the rate at which requests are processed to protect resources from being overwhelmed.
- **Data Partitioning:** Divides a database into smaller, more manageable pieces, which can be distributed across multiple servers to improve performance.
- **Multi-Tenancy:** Supports multiple customers (tenants) on a shared infrastructure while keeping their data isolated from each other.
- **Cloud Storage Gateway:** Provides seamless integration between on-premises infrastructure and cloud storage, allowing data to be moved to the cloud as needed.
- **Cloud Queue:** Manages asynchronous processing of tasks by placing tasks in a queue to be processed by available resources.
- **Stateless Application:** Designs applications so that they do not store client-specific data between requests, making them easier to scale in cloud environments.

## 11. Data Management Patterns

- **Data Replication:** Copies data across multiple systems to ensure availability and reliability.
- **Data Sharding:** Divides a large dataset into smaller chunks, called shards, that can be distributed across multiple databases or servers.
- **Event Sourcing:** Stores the state of a system as a sequence of events rather than just the final state, allowing for full history and audit trails.
- **CQRS (Command Query Responsibility Segregation):** Separates read and write operations into different models to optimize performance and scalability.
- **Master-Slave Replication:** A master database handles write operations, while one or more slave databases handle read operations to distribute the load.
- **Data Cache:** Stores frequently accessed data in a fast, in-memory cache to improve response times and reduce load on the primary database.
- **Data Warehousing:** Aggregates data from multiple sources into a central repository for analysis and reporting.
- **Data Lake:** Stores large amounts of raw data in its native format, typically used for big data analysis.
- **Indexing:** Creates indexes on data fields to speed up query performance by allowing faster data retrieval.

## 12. User Interface Patterns

- **Model-View-Controller (MVC):** Separates the application logic, user interface, and input control into three interconnected components, improving modularity and ease of maintenance.
- **Model-View-ViewModel (MVVM):** Extends MVC by introducing a ViewModel that handles data binding between the View and the Model, commonly used in modern front-end frameworks.
- **Observer:** Allows one or more objects to observe changes in another object, commonly used in user interface design to update the UI automatically when the data changes.
- **Command:** Encapsulates user actions as objects, allowing for actions like undo/redo and making it easier to manage user inputs.
- **Facade:** Provides a simplified interface to a complex subsystem, making it easier for users to interact with the system.
- **Template View:** Defines a template that outlines the structure of the user interface, allowing different views to share a common layout or behavior.
- **Responsive Design:** Ensures that the user interface adapts to different screen sizes and devices, providing an optimal experience across platforms.
- **Lazy Loading:** Delays the loading of non-essential resources until they are needed, improving the initial load time of the application.
- **Modal Window:** Uses overlay windows to focus the user's attention on a specific task or information, commonly used for dialogs or notifications.
- **Infinite Scroll:** Continuously loads new content as the user scrolls down the page, enhancing user experience by avoiding pagination.

## Principles

### SOLID Principles
- **Single Responsibility Principle (SRP):** A class should have only one reason to change, meaning it should have only one job.
- **Open/Closed Principle (OCP):** Objects or entities should be open for extension but closed for modification.
- **Liskov Substitution Principle (LSP):** Objects of a superclass shall be replaceable with objects of its subclasses without breaking the application.
- **Interface Segregation Principle (ISP):** No client should be forced to depend on methods it does not use.
- **Dependency Inversion Principle (DIP):** High-level modules should not depend on low-level modules; both should depend on abstractions.

### Other Foundational Principles
- **DRY (Don't Repeat Yourself):** Encourages the reduction of repetition within code.
- **KISS (Keep It Simple, Stupid):** Advocates for simplicity in design.
- **YAGNI (You Aren't Gonna Need It):** Focuses on adding functionality only when it is necessary.
- **Law of Demeter (LoD) or Principle of Least Knowledge:** Promotes minimal knowledge of an object beyond its immediate dependencies.
- **Composition Over Inheritance:** Prefers object composition over class inheritance for reusing code.
- **Inversion of Control (IoC):** Inversion of Control decouples the execution of tasks from their implementation, giving control over to the framework or infrastructure components. It's closely related to DIP as it involves relying on abstraction rather than concrete implementations.
