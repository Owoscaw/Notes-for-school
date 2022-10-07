The length of an activity represents the time it takes to complete. Weights can be added to arcs in an activity network to represent this. 

The early event time is the earliest time of arrival at the event that allows for the completion of all preceding activities. The late event time is the lastest time at which the event can happen without extending the total time needed for the project. Critical activities are activies that need to happen immediatley after each other, they have the same early and late event times.

Early event times are calculated starting from the source nodes and workinn towards the sink node, maximising the wieght of the path that reaches any event node. Note that direction applies. This is known as the forward pass.

Late event times are calculated working from the sink node towards the source node, minimising the path from the sink node to any event node. Note that the inverse of the direction of an activity applies. This is known as the backward pass.

The float of an activity represents the total amount of time an activity can be delayed without affecting the total duration of the project. It is given by the late event time - duration - early event time.