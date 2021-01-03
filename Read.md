## Longest Remaining Time First (LRTF)

1. This algorithm schedules those processes first which have the longest processing time remaining for completion. 

2. This algorithm can also be called the preemptive version of the  Longest Job First  Scheduling algorithm. 

<br>
# Procedure:

1. **Step-1:** First, sort the processes in increasing order of their Arrival Time.

2. **Step-2:** Choose the process having least arrival time but with most Burst Time. Then process it for 1 unit. Check if any other process arrives upto that time of execution or not.

3. **Step-3:** Repeat the above both steps until execute all the processes.

**Example:-** Consider the Following table of arrival time and burst time for four processes P1, P2, P3 and P4.

| Process Id | 	Arrival Time|	 Burst Time |
| :---:  |    :----:|   :----:|
| P1 |	 1 |	 2 |
| P2 |	 2 |	 4 |
| P3 |	 3 |	 6 |
| P4 |	 4 |	 8 |


### Steps:


1. **Note:-** that CPU will be idle for 0 to 1 unit time since there is no process available in the given interval.

2.  First executes all the process by 1 unit here we have four processes executes four processes orderly by their arrival time.

3. After 1 unit of execution of the process, the burst time will be reduced by 1.

| Process Id | 	Arrival Time|	 Burst Time |
| :---:  |    :----:|   :----:|
| P1 |	 1 |	 1 |
| P2 |	 2 |	 3 |
| P3 |	 3 |	 5 |
| P4 |	 4 |	 7 |

4. Then see which process burst time is high again execute the process by 1 unit.

5. both process burst time is the same, here which process Arrival time is low, execute that process.

| Process Id | 	Arrival Time|	 Burst Time |
| :---:  |    :----:|   :----:|
| P1 |	 1 |	 1 |
| P2 |	 2 |	 3 |
| P3 |	 3 |	 5 |
| P4 |	 4 |	 5 |

6. then repeat the all process.


## Gant Chart:
<img src="8.png" width="900" height="60" >

Turn Around Time (TAT)
= (Complition Time) - (Arival Time)

Also, Waiting Time (WT)
= (Turn Around Time) - (Burst Time) 

| Waiting Time |Turn Arround Time|Completion Time| Process Name | 
| :---:  |    :----:|   :----:|:----:|
| 15 |	 17 |	 18 | P1 |
| 13 |	 17 |	 19 | P2 |
| 11 |	 17 |	 20 | P3 |
| 9 |	 17 |	 21 | P4 |


Total Turn Around Time = 68 ms
So, Average Turn Around Time = 68/4 = 17.00 ms

And, Total Waiting Time = 48 ms
So Average Waiting Time = 48/4 = 12.00 ms 

### Advantages-
 
 1. No process can complete until the longest job also reaches its completion.
2. All the processes approximately finishes at the same time.

### Disadvantages-

1. The waiting time is high.
2. Processes with smaller burst time may starve for CPU.








