
## Scheduling 

  Scheduling is a Process of Determining which process will own CPU for execution while another process is on hold. Scheduling is to make sure that whenever the CPU remains idle, the OS at least select one of the processes available in the ready queue for execution. The selection process will be carried out by the CPU scheduler. It selects one of the processes in memory that are ready for execution.

  ### Types of Scheduling
1. Preemptive Scheduling
2. Non-Preemptive Scheduling

**Preemptive Scheduling**
The tasks are mostly assigned with their priorities. Sometimes it is important to run a task with a higher priority before another lower priority task, even if the lower priority task is still running. The lower priority task holds for some time and resumes when the higher priority task finishes its execution.

**Non-Preemptive Scheduling**
In this type of scheduling method, the CPU has been allocated to a specific process. The process that keeps the CPU busy will release the CPU either by switching context or terminating. It is the only method that can be used for various hardware platforms. That's because it doesn't need special hardware (for example, a timer) like preemptive scheduling.


## Why Scheduling Need

1. In a Single-processor system, Only one process can run at a time.
2. Any others must wait until the cpu is free and can be resheduled.
3. The objective of multiprogramming is to have some process running at all times, to maximize cpu utilization.
4. A process is executed until it must wait, typically for the completion of some I/O request.
5. In a simple computer system, the cpu then just sits idle All this waiting time is wasted no useful work is accomplished.



### Types of CPU scheduling Algorithm
 **There are mainly six types of process scheduling algorithms**

1. First Come First Serve (FCFS)
2. Shortest-Job-First (SJF) Scheduling
3. Shortest Remaining Time
4. Priority Scheduling
5. Round Robin Scheduling
6. Multilevel Queue Scheduling
