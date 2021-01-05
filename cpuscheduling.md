## CPU SCHEDULING  
* CPU scheduling is the basis of multiprogrammed operting system.  By switching the CPU among processes,  
* Which allows one process to use the CPU while the execution of another process is on hold(in waiting state) due to unavailability of any resource like I/O etc.  
* The aim of CPU scheduling is to make the system efficient,fast and fair.   
## BASIC CONCEPTS  
* In a single-processing system,only one process can run ata a time;any others must wait until the CPU is free and can be rescheduled.  
* In a multiprogramming is to have some process running at all times. to maximize CPU utilization.All this waiting time is wasted.  
* When one process has to wait,the operating system takes the CPU away from that process and gives the CPU to another process.this pattern continues.Every time one process has to wait,another process can take over use of the CPU.  
1.CPU brust  
2.I/O burst  
  EXAMPLE:  
  CPU brust-load store,add store,read from file.  
  I/O brust-wait for I/O.  
  CPU brust-store increment index write to file.  
  I/O brust-wait for I/O.    
 **Alternative sequence of CPU and I/O bursts**
## CPU SCHEDULING:DISPATCHER  
* The dispatcher is the module that gives control of the CPU to the process selected by the short-term scheduler.  
## Function  
1.Switching context  
2.Switching to user mode  
3.Jumping to the proper location in the user program to restart the program from where it left last time.  
  
  The time taken by the dispatcher to stop one process and start another process is known as the Dispatch latency.  
  ## TYPES OF CPU SCHEDULING  
  1.When a process switches from the **running** state to the **waiting** state(For I/O request of wait for the termination of one of the child processes)   
  2.When a process switches from the **running** state to the **ready** state(Eg:when an interrupt occurs)  
  3.When a process switches from the **waiting** state to the **ready** state(Eg:completion of I/O)  
  4.When a process **terminates**.  
  ## PREEMPTIVE AND NON-PREEMPTIVE  SCHEDULING
  ### Preemptive scheduling  
  * The tasks are usually assigned with priorities. At times it is necessary to run a certain task that has a higher priority before another task although it is running.when the priority task has finished its execution.  
  ### Non-preemptive scheduling  
* Once the CPU has been allocated to a process,the process keeps the CPU until it release the CPU either by terminating or by switching to the waiting state.  
* It is the only method that can be used on certain hardware platform,because it does not require the special hardware(Eg:a timer) needed for preemptive scheduling.  
## CPU SCHEDULING:SCHEDULING CRITERIA  
There are many different criteria to check when considering the **best** scheduling algorithm  
1.CPU utilization  
2.Throughput  
3.Turnaround Time  
4.Waiting Time  
5.Load Average  
6.Response Time  
## SCHEDULING ALGORITHMS  
1.FCFS Scheduling   
2.SJF Scheduling  
3.Priority Scheduling  
4.RR (Round Robin) Scheduling    
5.Multilevel Queue Scheduling    
6.Multilevel Feedback Queue Scheduling    
## ROUND ROBIN SCHEDULING  
* It is designed especially for time sharing systems. It is similar to FCFS scheduling,but preemption is added to enable the system to switch betwwen processes.  
* A small unit of time,called a **time quantum** or time slice,It is generally from 10 to 100 milliseconds length.  
It treat as circular queue allocate CPU scheduling time interval upto 1 time quantum.  
* A process may have a CPU burst of  less than 1 quantum. In this case,process itself will release the CPU voluntarily.The scheduler will then proceed to the next process in the ready queue.Otherwise,  
* If the CPU burst of the currently running process is longer than 1 time quantum,the timer will go off and will cause an interrupt to the operating system.A context switch will be executed,and the process will be put at the **tail** of the ready queue.  
## CONTEXT SWITCHING  
* The context switch is switching one process to another process,means saving the state old of process and loading saved state function in new process 
## PROCESS CONTROL BLOCKS    
* The process is stored in process control blocks.  
* Information to be stored for context switching in PCB is:  
1.Program counter  
2.Scheduling information  
3.Changed state  
4.Accounting information  
5.Base and Limit register


For Example:  

Process | Arrival Time | Burst time
---------|----------|---------
 p1 | 3 | 5  
 p2 | 0 | 8
 p3 | 1 |  7 
 p4|  2 |10  
   
    Quantum time=4 milliseconds
p2->0-4 (P2 reamaining 4 BT)  
P3->4-8(P3 Remaining 3 BT)  
p4->8-12(p4 Remaining 6 BT)  
P1->12-16(P1 Remaining 1 BT)  
P2->16-20(P2 Finished BT)   
P3->20-23(P3 Finished BT)    
P4->23-27(P4 Remaining 2 BT)  
P1->27-28(P1 Finished BT)    
P4->28-30(P4 Finished BT)      

  Process | Arrival Time | Burst time | Completion time | Turn around time |waiting time
---------|----------|---------|-------|------|-----
 p1 | 3 | 5  |28 |25|20
 p2 | 0 | 8  | 20|20|12
 p3 | 1 |  7 | 23|22|15 
 p4|  2 |10  | 30|28|18
### Average waiting time for the above schedule  
 
=16.25 milliseconds.  
### Average turn around time for the above schedule  
 
=23.75 milliseconds.   
## ADVANTAGES   
* RR is a preemptive schedulers.  
* Every process gets an equal share of the CPU.RR is cyclic in nature,so there is no starvation 
## DISADVANTAGES   
* If the time quantum too short,increase the overhead and lowers the CPU efficiency.  

* If the time quantum is too large,RR scheduling degenerates to an FCFS policy.




