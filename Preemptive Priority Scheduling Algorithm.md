## Pre-emptive Priority Scheduling Algorithm
-	Each process is assigned a priority. Process with highest priority is to be executed first and so on
-	Process with same priority is executed on first come first serve basis.
-	Priority can be decided based on memory requirements, time requirements or any other resource requirement

-	Sometimes it is important to execute higher priority tasks immediately even when a task is currently being executed. 
For example, when a phone call is received, the CPU is immediately assigned to this task even if some other application is currently being used. This is because the incoming phone call has a higher priority than other tasks. This is a perfect example of priority pre-emptive scheduling. If a task with higher priority than the current task being executed arrives then the control of the CPU is taken from the current task and given to the higher priority task.

Examples
1.	Calculate the average waiting time and average turnaround time for the following set of the process using pre-emptive priority scheduling


Process | Burst time  | Priority | Arrival time
--------|-------------|----------|-------------
P1	    |6	          |2	     |0
P2	    |2	          |2	     |1
P3	    |3	          |4	     |1
P4	    |1	          |1	     |2
P5	    |2	          |3	     |2


  Arrival | P1 | P2 | P3 | P4 | P5
 --|----|----|----|----|---
 0 | 2  |    |    |    | 
 1 | 2  |  2 | 4  |    | 
 2 | 2  |  2 | 4  |  1 | 3


### Gantt chart
1    1  	1	4	 2    2   3        				
P1 | P1 | P4 | P1 | P2 | P5 | P3
---|----|----|----|----|----|---
0  1    2    3	  7    9    11  14	


Process | Burst time | Arrival time  |Completed time | Turnaround time (completed time – Arrival time) | Wasting time (Turnaround -Burst time)
------- | ------- | ------- | ------- | ------- | -------
P1 | 6  | 0       | 7       | 1       | 7
P2 | 2  | 1       | 9       | 6       | 8
P3 | 3  | 1       | 14      | 10      | 13
P4 | 1  | 2       | 3       | 0       | 1
P5 | 0  | 2       | 11      | 7       | 9  
    Average Waiting time = 24/5=4.8
    Average Turnaround time = 38/5 = 7.6
---------------------------------------------------------------------------------------------


2.	Calculate the average waiting time and average turnaround time for the following set of the process using pre-emptive priority scheduling

Process | Burst time  | Priority | Arrival time
--------|-------------|----------|-------------
P1	    |2	          |2	    |2
P2	    |1	          |3	    |0
P3	    |3	          |4	    |1
P4	    |5	          |1	    |3
P5	    |4	          |5	    |4



 Arrival | P1 | P2 | P3 | P4 | P5
 --|----|----|----|----|---
 0 |    | 3  |    |    | 
 1 |    |    | 4  |    | 
 2 | 2  |    | 4  |    | 
 3 | 2  |    | 4  | 1  | 
 4 | 2  |    | 4  | 1  | 5


## Gantt chart
1  1	1    1    1	   3	1    2    4  
P2 | P3 | P1 | P4 | P4 | P4 | P1 | P3 | P5
---|----|----|----|----|----|----|----|---
0  1    2    3	  4    5	8    9   11  15	  


Process | Burst time | Arrival time  |Completed time | Turnaround time (completed time – Arrival time) | Wasting time (Turnaround -Burst time)
------- | ------- | ------- | ------- | ------- | -------
P1 | 2  | 2       | 9      | 7       | 5
P2 | 1  | 0       | 1      | 1       | 0
P3 | 3  | 1       | 11     | 10      | 7
P4 | 5  | 3       | 8      | 5       | 0
P5 | 4  | 4       | 15     | 11      | 7  

	
Average Waiting time =19/5 = 4.8  
Average Turnaround time = 34/5=6.8


#### Advantage
-	Priority is considered, Critical process can get even better response time.

#### Disadvantage
-	Starvation is possible for low priority process. It can be overcome by using called Aging
-	Aging gradually increase the priority of process that wait in the system for a long time 


