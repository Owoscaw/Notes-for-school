An activity network is a [[Graph theory|graph]] that represents the activities that need to be done and how long they take. Each activity is represented by its own arc. All events have to start from one or more event or the source. All events have to end at one or more event or the sink. The source, sink, and all places where two events meet are nodes. The earliest time that a project can be completed is known as the project's earliest completion time, or critical time.

Dummy activities are arcs that represent no activity and have no weight. They are used to maintain exclusive dependance. For example if activity $C$ is dependent on activities $A$ and $B$, however activity $D$ is dependent only on $A$, a dummy is needed from the node at $A$ and $D$ to the node at $B$ and $C$ to maintain this logic.

## Early and late times:

Each node has an associated early and late time that represents the earliest and latest times a preceding activity can start. If a node has the same early and late time, it is critical. 

The early event time is the earliest time of arrival at the event that allows for the completion of all preceding activities. The late event time is the lastest time at which the event can happen without extending the total time needed for the project. Critical activities are activies that need to happen immediatley after each other, they have the same early and late event times.

Early event times are calculated starting from the source nodes and workinn towards the sink node, maximising the wieght of the path that reaches any event node. Note that direction applies. This is known as the forward pass.

Late event times are calculated working from the sink node towards the source node, minimising the path from the sink node to any event node. Note that the inverse of the direction of an activity applies. This is known as the backward pass.

The float of an activity represents the total amount of time an activity can be delayed without affecting the total duration of the project. It is given by the late event time - duration - early event time.

## Lower bound:

Practically, there will be a finite amount of workers availible to complete the tasks laid out in an activity network. A lower bound for the amount of workers needed can be found by rounding up the sum of all activity times, divided by the critical time:
$$\Huge lower\,\,bound=\left\lceil\frac{\sum event\,\,times}{critical\,\,time}\right\rceil$$