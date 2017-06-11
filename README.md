# A Framework for Reactive Systems in Go
![Image of mascot](images/mascot.png)
During the last decade, the rise of disruptive, cutting-edge technologies was shaking up
the developer communities in the field of computer science. The top dogs among the
technology leaders were using their own developments to cope with massive data streams
and high customer expectations about responsiveness. These systems are described
concisely as Reactive Systems in [The Reactive Manifesto](http://www.reactivemanifesto.org). Nowadays, these systems
are known as cloud and offered as a service (aaS).

At the same time, the price reduction of edge devices leads to another major topic, IoT.
But the expected scenarios in IoT seem to be only partially manageable by the approach
of current cloud technology. Mainly due to two reasons, the further increase of the data
magnitudes and the demands of time critical applications.

As an obvious consequence, the top architecture has to be transformed once again from
a more centralized approach to a decentralized and distributed one.

### Reactive Systems

```
"We believe that a coherent approach to systems architecture is needed, and we believe
that all necessary aspects are already recognised individually: we want systems that are
Responsive, Resilient, Elastic and Message Driven. We call these Reactive Systems."
```
*Jonas Bonér, Dave Farley, Roland Kuhn, and Martin Thompson, [The Reactive Manifesto](http://www.reactivemanifesto.org)*

Systems built as Reactive Systems are traditionally acting as a server providing func-
tionality to other clients. They are the cloud, and the clients are the edge.

### go-reactive

A set of connected isomorphic applications having a server and a client shape can act as
a Reactive System in a decentralized manner.

From the client perspective, the Reactive System is accessible via Go’s CSP-style con-
current programming features. From the server perspective, the application is listening
for requests to handle being part of the Reactive System. That means, in contrast to
classic client-server models, the server functionality gets distributed over the isomorphic
applications being the Reactive System. This approach does not need a hierarchical
structure.

### Approach
Make the applications a Reactive System will take place in a certain order using well-
known technologies and methods, respectively:

##### Message Driven
Message Driven is the groundwork of a Reactive System. Unlike Event Driven, Message
Driven relies only on the messages flowing through the system ignoring the sender.

##### Elastic
Elasticity is the ability to scale, precisely to delegate tasks to other participants of the
system. Because of the lack of hierarchy, no start or shutdown can be triggered from
others. Instead, a stand-by of applications is published waiting to take over tasks on
request.

##### Resilient
Resilience is the ability to handle failures and even outages of system’s participants
transparently. Other applications on stand-by will be triggered to fill in accordingly.
Therefore a heartbeat-like mechanism keeps the system up to date.

##### Responsive
Additional to the system properties mentioned above, responsiveness will be ensured
by a well-known, high available naming service and a broadcast mechanism for ad-hoc
systems in isolated areas.

##### gRPC and Protocol Buffer
[gRPC](http://www.grpc.io), the RPC implementation by Google, and [Protocol Buffer](https://developers.google.com/protocol-buffers), a serializing
framework for structured data, will be used in combination to realize the communication
layer of the Reactive System.

##### Test-Driven Development
Implementation and testing will be combined as known from the methodology of Test-
Driven Development.

##### SOLID Refactoring
Finally, the package will be refactored to optimize the API and by the SOLID principles
applied to Go:
 - **S**ingle responsibility principle
 - **O**pen/closed principle
 - **L**iskov substitution principle
 - **I**nterface segregation principle
 - **D**ependency inversion principle
