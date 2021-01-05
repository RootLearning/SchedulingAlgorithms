## First Come First Serve Scheduling

In this algorithm, the process that comes first in the ready queue is scheduled to the CPU.

It is managed by the FIFO queue.

When the process comes first in the ready queue, its PCB linked to the tail.

When the CPU is free, the first process is allocated to the CPU.

The running process is then removed from the queue.

**EXAMPLE PROBLEM**:

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

### SOLUTION:



Process | Arrival Time| Waiting Time | Completion Time | Turn around
--------|---------|---------|------------|-----------
P1 | 2 | 7 | 10 | 8
P2 | 3 | 10 | 14 | 11
P3 | 1 | 2 | 7 | 6
P4 | 0 | 0 | 2 | 2
Average Time |  | 19 |  | 27

**Average Waiting Time**:

19/4=4.75 miliseconds.

**Average TurnAround Time**:

27/4=6.75 milliseconds.


### ADVANTAGES:

* This is the simplest algorithm.

* Easy to Understand.

* Every process will get a chance to run, so starvation doesn't occur.

### DISADVANTAGES:

* Average waiting time in this algorithm is quite long comparatively.

* If the first process has a long CPU burst time and other processes have a short burst time, the shorter process has to wait unnecessarily for the first longer process to end.

* This results in Convey Effect.

* This effect leads to lower CPU utilization.

### Convey Effect Problem:


Process | Arrival Time | Burst Time
--------|--------------|-----------
P1 | 2 | 1
P2 | 0 | 20
P3 | 3 | 2
P4 | 1 | 1

In this problem,we can clearly see that the first arrived process has  long burst time and the following process have small burst time.

In this cases,the waiting time for the small burst time process is going to be too long.

### SOLUTION:

p2 | p4 | p1| p3
----|-----|-----|-----





PROCESS | ARRIVAL | WAITING | COMPELTION | Tur around
--------|---------|---------|------------|-----------
P1 | 2 | 21 | 22 | 20
P2 | 0 | 0 | 20 | 20
P3 | 3 | 22 | 24 | 21
P4 | 1 | 20 | 21 | 20
Average Time |  | 63 |  | 81

**Average Waiting time:**

63/4=15.15 milliseconds.


**Average TurnAround Time:**
81/4=20.25 milliseconds.

Thus,it will affect the performance of CPU and consider to be a worst algorithm of all.





























