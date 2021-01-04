# Multilevel Queue Scheduling :

* Ready queues are divided into  different classes ,that classes has a different own scheduling.
* For example, foreground(interactive) process and background(batch) process. These classes needs a different shecduling.
* In a processes has a different types of scheduling queues, at that kind of situation Multilevel Queue scheduling needed.
* The foreground queue can be scheduled by using a round-robin algorithm while the background queue is scheduled by a first come first serve algorithm


  Ready Queue is divided into separate queues for each class of processes. For example, let us take three different types of process System processes, Interactive processes and Batch Processes. All three process have there own queue.

    **HIGH PRIORITY** <-------------> **LOW PRIORITY**

              |System processes     |---> Queue 1

              |Interactive processes|---> Queue 2

              |Batch processes      |---> Queue 3

  All three different type of processes have there own queue. Each queue have its own Scheduling algorithm. Queue 1 and Queue 2 uses Round Robin and Queue 3 can use FCFS to schedule there processes. 

* The scheduled between the queues which are easily implemented as a fixed- priority preemptive scheduling.

**Fixed priority preemptive scheduling method :**
             1. Let us consider following priority order queue 1 - queue 2 - queue 3.
             2. According to this algorithm the batch process can run when the system process and interactive process are empty.
             3.And when the batch process is running and the system process or interative process are arriving to process at that time batch process can be preempted.

**Example Program :**

Consider below table of four processes under Multilevel queue scheduling.

Process | Arrival Time | Burst Time|Queue Number
---------|----------|---------|------------|
 P1 | 0 | 4 | 1
 P2 | 0 | 6 | 1
 P3 | 1 | 10 | 2
 P4 | 10 | 7 | 2
 P5 | 9 | 8 | 1

 Priority of queue 1 is greater than queue 2. queue 1 uses Round Robin (Time Quantum = 2) and queue 2 uses FCFS. 

Below is the gantt chart of the problem : 

![granttchart](grantt.PNG)

 At the starting of both Queue have process in process in Queue runs first because of high priority and process in Round Robin and completes 10 units of process time and queue two have to run and between of the process P5 is arriving (arriving time 15), so the queue two has stop in time 15 and starting the  queue one's process , when the process can be empty int the queue one. Then the queue two can be processed in there own scheduling.


**Advantages**:

* Permanently assigned to the queue.
* It has advantage of low scheduling overhead.

**Disadvantages**:

* Some processes may starve for CPU if some higher priority queues are never becoming empty.
* It is inflexible in nature.