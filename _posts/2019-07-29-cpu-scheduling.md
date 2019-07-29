---
layout : post
title : CPU Scheduling Simulator
---

### 2019 Operating System Term Project



#### Project title : CPU Scheduling Simulator

In this project, I implemented several CPU scheduling algorithms in C. CPU scheduling is one of the most important functions of Operating System.<br>

I built a simulator in C which can run for 10 different algorithms and you can evaluate the performance of those algorithms. **FCFS, preemptive FCFS, preemptive SJF, nonpreemptive SJF, preemptive Priority, nonpreemptive Priority, Round Robin, RR with priority, RR with SJF, Multi-Level Feedback Queue** are the cpu scheduling algorithms I have implemented.<br>

The performance metrics are **average waiting time, average turnaround time, average response time and utilization**.
Through these metrics, you can compare one algorithm with others and analyze each of them.<br>

There is a report of this project [here](https://github.com/limhyesu98/OperatingSystem_cpuSchedule/blob/master/Term_Report_OS.pdf).
It includes explanation of basic concept of the cpu scheduler and cpu scheduling algorithms. 
Also, it contains explanation of how I implemented the simulator, and the result of running each algorithm with 3 different processes.<br>

The code of this simulator is [here](https://github.com/limhyesu98/OperatingSystem_cpuSchedule/blob/master/Term_Code_OS.c).
