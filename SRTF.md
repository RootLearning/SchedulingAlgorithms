## Shortest Remaining Time First
+	Shortest Remaining Time First Algorithm is the **preemptive version** of **SJF scheduling**.
+	In SRTF, the execution of the process can be stopped after certain amount of time.
+ 	At the arrival of every process, the short term scheduler schedules the process with the least remaining burst time among the list of available processes and the running process.
+ Once all the processes are available in the ready queue.   No preemption will be done and the algorithm will word as Shortest Job First (SJF) Scheduling.
+ The context of the process is saved in the Process Control Block (PCB) when the process is removed from the execution and the next process is scheduled.
+ If the next CPU bursts of two processes are the same, First Come and First Served (FCFS) scheduling is used to break the tie.
+ This PCB is accessed on the next execution of this process.

#### Example for Shortest Remaining Time First (SRTF)
|Process Id|Arrival Time|Burst Time|
|---|---|---|
|P1|0|8|
|P2|1|4|
|P3|2|9|
|P4|3|5|

**Stop 0 :**  At time = 0, P1 (8) Arrives start the execution.
  
**Gantt Chart**
|P1|
|--|
**Stop 1 :** At time=1, P2 (4) Arrives and executed because it’s burst time lesser than P1 (8-1=7).  P1 is preempted and P2 starts the execution.
|P1|P2|
|--|--|
**Stop 2 :** At time=2, P3 (9) arrives and it’s compared to P1 (7) and P2 (3).  P3 is added to the ready queue.  P2 will continue the execution.
|P1|P2|P2|
|--|--|--|
**Stop 3 :**  At time=3, P4(5) arrives and its’s compared to P1(7) , P2 (2) and P3 (9).  P4 is added to the ready queue.  P2 will continue the execution.
|P1|P2|P2|P2|
|--|--|--|--|
**Stop 4 :** At time=5, Process P2 will finish it’s execution.  The Burst time of P1, P3 and P4 Compared.  Process P4 is executed because its burst time is the lowest.
|P1|P2|P2|P2|P2|P4|
|--|--|--|--|--|--|
**Stop 5 :** At time=10, Process P4 will finish it’s execution.  The Burst time of remaining processes are P1 and P3 Compared.  Lowest burst time of Process P1 (8-1) starts the execution.
|P1|P2|P2|P2|P2|P4|P1|
|--|--|--|--|--|--|--|
**Stop 6 :**  At time=17, Process P1 will finish its execution.  The remaining process P3 will starts the execution.
|P1|P2|P2|P2|P2|P4|P1|P3|
|--|--|--|--|--|--|--|--|
**Stop 7 :**  At time=26, Process P3 will finish its execution.

**Process Time**
|Starting Time|P1|P2|P3|P4|
|--|--|--|--|--|
|0|8||||
|1|7|4|||
|2|7|3|9||
|3|7|2|9|5|
|4|7|1|9|5|
|5|7|0|9|5|
|6|7|0|9|4|
|7|7|0|9|3|
|8|7|0|9|2|
|9|7|0|9|1|
|10|7|0|9|0|
|11|6|0|9|0|
|12|5|0|9|0|
|13|4|0|9|0|
|14|3|0|9|0|
|15|2|0|9|0|
|16|1|0|9|0|
|17|0|0|9|0|
|18|0|0|8|0|
|19|0|0|7|0|
|20|0|0|6|0|
|21|0|0|5|0|
|22|0|0|4|0|
|23|0|0|3|0|
|24|0|0|2|0|
|25|0|0|1|0|
|26|0|0|0|0|

+ Waiting Time = Completion time - Burst Time - Arrival Time
+ Turn Around Time = Waiting time + Burst Time

|Process Id|Arrival Time| Burst Time|Completion Time|Waiting Time|Turn around Time|
|---|---|---|---|---|---|
|P1|0|8|17|17-8-0=9|9+8=17|
|P2|1|4|5|5-4-1=0|0+4=4|
|P3|2|9|26|26-9-2=15|15+9=24|
|P4|3|5|10|10-5-3=2|2+5=7|

**Average Waiting Time**
+ ==> (9+0+15+2) = 26
+ ==> 26/4 = 6.5
+ Average Waiting Time = 6.5

**Average Turnaround Time**
+ ==> (17+4+24+7) = 52
+ ==> 52/4 = 13
+ ==> Average Waiting Time = 13

## Advantages

1.	Specific process switches from the running state to the ready queue and alternatively.
2.	Process finished its execution and terminated.

## Disadvantages

1. Job completion time must be known earlier, but it is hard to predict.
2.	Hard to know the length of the upcoming CPU request.