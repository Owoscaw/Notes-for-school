## Gantt charts:

Gantt charts are used to model the activities in an [[Activity networks|activity network]]. They provide a graphical method of representing the range of early and late timesfor a project:
![[Gantt activity example.png|450]]
becomes:
![[Gantt example.png|500]]

## Resource Histograms:

A resource histogram is an extension of a Gantt chart in the sense that it provides a graphical representation of what needs to happen when, however now indicates how many workers are required for each activity and when they need to be working. Each worker cannot perform multiple activities at once, and once they have started an activity, they have to finish it. Once a worker finishes an activity, they will start the next one as soon as they can (no breaks).

Adjusting when activities start in order to take into account the contraints on workers is called resource leveling. This is used when there are fewer workers availible than the [[Activity networks|lower bound]] for earliest completion.

## Scheduling diagram:

A scheduling diagram is a way of assigning workers to activitys, graphically. Each activity is assumed to have one worker, and each worker is used as soon as they are availible. If there is a choice of activities that a worker may take, the lowest one is chosen by convention.