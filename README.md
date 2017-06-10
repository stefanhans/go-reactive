# go-reactive
## Framework for Reactive Systems in Go

During the last decade, the rise of disruptive, cutting-edge technologies was shaking up
the developer communities in the field of computer science. The top dogs among the
technology leaders were using their own developments to cope with massive data streams
and high customer expectations about responsiveness. These systems are described
concisely as Reactive Systems in [The Reactive Manifesto](http://http://www.reactivemanifesto.org). Nowadays, these systems
are known as cloud and offered as a service (aaS).

At the same time, the price reduction of edge devices leads to another major topic, IoT.
But the expected scenarios in IoT seem to be only partially manageable by the approach
of current cloud technology. Mainly due to two reasons, the further increase of the data
magnitudes and the demands of time critical applications.

As an obvious consequence, the top architecture has to be transformed once again from
a more centralized approach to a decentralized and distributed one.
A set of connected isomorphic applications having a server and a client shape can act as
a Reactive System in a decentralized manner.

From the client perspective, the Reactive System is accessible via Go’s CSP-style con-
current programming features. From the server perspective, the application is listening
for requests to handle being part of the Reactive System. That means, in contrast to
classic client-server models, the server functionality gets distributed over the isomorphic
applications being the Reactive System. This approach does not need a hierarchical
structure.
```
"We believe that a coherent approach to systems architecture is needed, and we believe
that all necessary aspects are already recognised individually: we want systems that are
Responsive, Resilient, Elastic and Message Driven. We call these Reactive Systems."
```
*Jonas Bonér, Dave Farley, Roland Kuhn, and Martin Thompson, [The Reactive Manifesto](http://http://www.reactivemanifesto.org)*

Systems built as Reactive Systems are traditionally acting as a server providing func-
tionality to other clients. They are the cloud, and the clients are the edge.