## First Come First Serve Scheduling

In this algorithm, the process that comes first in the ready queue is scheduled to the CPU.

It is managed by the FIFO queue.

When the process comes first in the ready queue, its PCB linked to the tail.

When the CPU is free, the first process is allocated to the CPU.

The running process is then removed from the queue.

EXAMPLE PROBLEM:

Process | Arrival time | Burst time
--------|--------------|-----------
P1 | 2 | 3
P2 | 3 | 4
P3 | 1 | 5
P4 | 0 | 2


In this FCFS algorithm, the processor will choose the process based on the arrival time(which process came first).

In the above example, the process P4 came first with an arrival time of 0.

 ### SOLUTION:

p4 | p3 | p1 | p2
----|-----|-----|-----



Process | Arrival Time| Process Time | Waiting Time
------- | ------- | ------- | -------
P4 | 0 | 0-2 | 0
P3 | 1 | 2-7 | 2
P1 | 2 | 7-10 | 7
P2 | 3 | 10-14 | 10

#### Average Waiting Time:

0+2+7+10=19

19/4=4.75

Average Waiting Time=4.75ms


### ADVANTAGES:

* This is the simplest algorithm.

* Easy to Understand.

* Every process will get a chance to run, so starvation doesn't occur.

### DISADVANTAGES:

* Average waiting time in this algorithm is quite long comparatively.

* If the first process has a long CPU burst time and other processes have a short burst time, the shorter process has to wait unnecessarily for the first longer process to end.

* This results in Convey Effect.

* This effect leads to lower CPU utilization.


