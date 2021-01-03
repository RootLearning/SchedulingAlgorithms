# Non-Preemptive Priority Scheduling Algorithm.

Non-Preemptive Priority Scheduling Algorithm is one of the most common scheduling algorithms in batch systems. Each process is assigned first arrival time (less arrival time process first) if two processes have same arrival time, then compare to priorities (highest process first). Also, if two processes have same priority then compare to process number (less process number first). This process is repeated while all process get executed.

**Selection Criteria:** The process, that has highest priority, is served first.  
**Decision Mode:** Non Preemptive: Once a process is selected, it runs until it blocks for an I/O or some event, or it terminates.  
**Implementation:** This strategy can be implemented by using sorted FIFO queue. All processes in a queue are sorted based on their priority with highest priority process at front end. When CPU becomes free, a process from the first position in a queue is selected to run.  

**Example:** Consider the following set of seven processes. Their arrival time, total time required completing the execution and priorities are given in following table. Consider all time values in millisecond and small values for priority means higher priority of a process.

Process | Arrival Time | Burst Time | Priority
--------|--------------|------------|---------
P1 | 0 | 8 | 3
P2 | 1 | 2 | 4
P3 | 3 | 4 | 4
P4 | 4 | 1 | 5
P5 | 5 | 6 | 2
P6 | 6 | 5 | 6
P7 | 10 | 1 | 1

After Gantt chart calculation the following is prepared:

Process | Arrival Time | Burst Time | Priority | Completion Time | Turnaround Time | Waiting Time | Response Time
--------|--------------|------------|----------|-----------------|-----------------|--------------|--------------
P1 | 0 | 8 | 3 | 8 | 8 | 0 | 0
P2 | 1 | 2 | 4 | 17 | 16 | 14 | 14
P3 | 3 | 4 | 4 | 21 | 18 | 14 | 14
P4 | 4 | 1 | 5 | 22 | 18 | 17 | 17
P5 | 5 | 6 | 2 | 14 | 9 | 3 | 3
P6 | 6 | 5 | 6 | 27 | 21 | 16 | 16
P7 | 10 | 1 | 1 | 15 | 5 | 4 | 4

Average Turnaround Time = 95/7 = 13.5

Average Waiting Time = 68/7 = 9.7



**Key Note:**  
**Non-Preemptive Scheduling**:
Non-preemptive Scheduling is used when a process terminates, or a process switches from running to waiting state. In this scheduling, once the resources (CPU cycles) is allocated to a process, the process holds the CPU till it gets terminated or it reaches a waiting state. In case of non-preemptive scheduling does not interrupt a process running CPU in middle of the execution. Instead, it waits till the process complete its CPU burst time and then it can allocate the CPU to another process.