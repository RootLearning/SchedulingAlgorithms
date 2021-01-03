## Process Scheduling
+ CPU scheduling is the basis of multiprogrammed operating systems.  By swithing the CPU among processes, the operating system can make the computer more productive.
+ When one process has to wait, the operating system takes the CPU away from that process and gives the CPU to another process.
#### CPU-I/O Burst Cycle
+ Process execution consists of a cycle of CPU execution and I/O wait.  Processes alternate between these two states.
+ Process execution begins with a **CPU Burst**.
+ Followed by an I/O Burst, which is followed by another CPU Burst and so on.  Even final CPU burst ends with a system request to terminate execution.

#### CPU Scheduler
+ Whenever the CPU becomes idle, the operating system must select one of the processes in the ready queue to be executed. 
+ The Selection process is carried out by the **Short-term scheduler**.
+ The scheduler selects a process from the processes in memory that are ready to execute and allocates the CPU to that process.

### Preemptive Scheduling and Non-Preemptive Scheduling
+ When a process switches from the running state to the waiting state.
+ When a process switches from running state to ready state.
+ When a process switches from the waiting state to ready state.
+ When a process terminate.
+ Above there is no choice in terms of scheduling.  A new process must be selected for execution.  However, for situations 2 and 3.

+ When Scheduling takes place only under circumtances above points, we say that the scheduling scheme is **nonpreemptive** or **Cooperative**, Otherwise it is preemptive.

#### Scheduling Difference Criteria: 
* CPU utilization.
* Throughput
* Turnaround time.
* Waiting time.
* Response time.

### There are different types of algorithms available
+ CPU scheduling deals with the problem of deciding which of the processes in the ready queue is to be allocated the CPU. There are many different CPU-scheduling algorithms.
1. First-Come, First-Served Scheduling. (FCFS)
2. Shortest-Job-First Scheduling (SJF)
3. Shortest Remaining Time First (SRTF)
4. Longest Remaining Time First (LRTF)
5. Priority Scheduling
6. Round-Robin Scheduling
7. Multilevel Queue Scheduling
8. Multilevel Feedback Queue Scheduling