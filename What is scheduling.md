# What is Scheduling  

 
  
CPU scheduling is a process which allows one process to use the CPU while the execution of another process is on hold (in waiting state) due to unavailability of any resource like I/O etc, thereby making full use of CPU. The aim of CPU scheduling is to make the system efficient, fast and fair.  

 For example, would it make sense to start your day by going to bed, then eating supper, then working for four hours, returning home to do laundry, then going back to work, and finally ending the day by having breakfast? This is a very inefficient and time-consuming way to spend your day!  

To make your day more logical and efficient, you work on a schedule. An operating system operates in a similar manner: by scheduling tasks, improving efficiency, reducing delays and wait times (response times to the system), and managing CPU resources better.


### Why we need scheduling
In Multiprogramming, if the long-term scheduler picks more I/O bound processes then most of the time, the CPU remains idol. The task of Operating system is to optimize the utilization of resources.
If most of the running processes change their state from running to waiting then there may always be a possibility of deadlock in the system. Hence to reduce this overhead, the OS needs to schedule the jobs to get the optimal utilization of CPU and to avoid the possibility to deadlock.

### Criteria for Scheduling
Criteria | Description
---------|------------
CPU Utilization | Reduces the strain on the CPU and manages the percentage of time the CPU is busy
Throughput | Increases the number of processes completed in a given time frame
Wait Time | Reduces the waiting time of a process 
Response  | Time Minimizes the time a user has to wait for a process to run
Turnaround Time | Total time a process takes to run, from start to finish (includes all waiting time)   
  
A process scheduler schedules different process to be assigned to the CPU based on particular scheduling algorithms. 
-	First come first served scheduling
-	Shortest job next scheduling 
-	Priority scheduling 
-	Shortest remaining time
-	Round robin scheduling
-	Multiple level queue scheduling    
These algorithms are either, non-preemptive or preemptive
------------------------------------------------------------------------
