## CPU SCHEDULING 

### **WHAT?**

In the multi-programmed operating system, when the CPU is idle, another process should be scheduled to the CPU to increase the utilization.

The main aim of the CPU scheduler is to avoid the  CPU idle state.

Every time one process has to wait, another process can take overuse of the CPU.

The main purpose of the CPU Scheduler is to decide which process should be allocated to the CPU.

### **WHY?**


To avoid the waiting time or CPU idle state.

The process execution consists of two-cycle:

* CPU EXECUTION
* I/O WAIT

#### **CPU EXECUTION**:

1. In this CPU execution, the process is being executed in the CPU.

#### **I/O WAIT**:

1. In this cycle, the process will be waiting for the I/O for further execution.

1. In this time, the CPU becomes idle.

2. In order to avoid this idle waiting time, the CPU scheduler schedule another process for the CPU.

3. Thus, the CPU is utilized to the fullest.

When the process goes to wait  state, the scheduler selects another process in the ready queue and allocates to the CPU.

### When the scheduler is required?

* When the process goes from execution state to the wait state.

* When the process terminated.

* In the above conditions, there are no choices in terms of scheduling. A new process should be selected for execution.

This is called ** Non-Preemptive scheduling**.

* In the Non-Preemptive Scheduling,once the CPU has been allocated to a process,the process keeps the CPU untils it release CPU either by termination or by switching to waiting state.


* When the process goes from execution to ready state

* When the process goes from wait state to ready state.

* In the above two conditions, there is the choice for scheduling.

This is called **Pre-emptive scheduling**.

In this, the process can be preempted before the termination or waiting state according to the time slots.

There are various types of algorithms are available for scheduling.

The algorithm has different properties and the scheduling criteria differ.

The different criteria are:

* CPU Utilization

* Response Time

* Throughput

* Turnaround Time

* Waiting Time

There are different types of algorithms available. Each algorithm focus on different criteria.


1. First Come First Serve,

2. Shortest Job First.

3. Round-Robin.

4. Priority Scheduling. 

5. Multi Level Queue Scheduling,

6. Multi Level Feedback  Queue Scheduling.

