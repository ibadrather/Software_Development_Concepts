# RESTful
Representational State Transfer (REST) is an architectural style for designing networked applications. It defines a set of constraints that, when applied as a whole, emphasizes scalability of component interactions, generality of interfaces, independent deployment of components, and intermediary components to reduce latency, enforce security, and encapsulate legacy systems.

Here are the key constraints according to the REST architecture:

**Client-Server**: The client-server constraint operates on the concept that the client and the server should be separate from each other and allowed to evolve individually. The separation of concerns helps improve the user interface portability across multiple platforms and enhance the server components' scalability by simplifying the server architecture.

**Stateless**: The communication between the client and the server must be stateless. This means that each request from the client to the server must contain all the necessary information for the server to understand and process the request. The server should not store any context between requests.

**Cacheable**: The network infrastructure should support and appropriately leverage caching to improve efficiency, scalability, and user-perceived performance by partially or completely eliminating some client-server interactions.

**Uniform Interface**: A uniform interface between components simplifies and decouples the architecture, which enables each part to evolve independently. The four constraints for this uniform interface are:

  - Identification of resources: Individual resources are identified in requests, for example using URIs in web-based REST systems.
  - Manipulation of resources through representations: When a client has a representation of a resource, including any metadata attached, it has enough information to modify or delete the resource.
  - Self-descriptive messages: Each message includes enough information to describe how to process the message.
  - Hypermedia as the Engine of Application State (HATEOAS): Clients deliver state via body contents, query-string parameters, request headers, and the requested URI. Services deliver state to clients via body content, response codes, and response headers.

**Layered System**: The layered system architecture allows an application to be more stable by limiting component behavior. This means that a client cannot ordinarily tell whether it is connected directly to the end server, or to an intermediary along the way.

**Code-On-Demand** (optional): Most of the time, RESTful services will be completely stateless. But when necessary, servers can transfer executable code to the client. This constraint is optional and, when used, usually in the form of applets or client-side scripts.

These constraints, when applied to a system, guide the system's architecture towards a more maintainable, scalable, and reliable design.

