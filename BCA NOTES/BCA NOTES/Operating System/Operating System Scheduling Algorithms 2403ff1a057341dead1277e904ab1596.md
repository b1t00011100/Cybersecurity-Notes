# Operating System Scheduling Algorithms

<aside>
💡 A Process Schedulers schedules different processes to be assigned to the CPU based on particular scheduling algorithms.

</aside>

### First Come First Serve (FCFS)

- Jobs are executed on first come, first serve basis.
- It is a non-preemptive, pre-emptive scheduling algorithm.
- Easy to understand, and implement
- Queue : FIFO
- Poor in performance as average wait time is high.

### Shortest Job Next (SJN)

- This is also known as **Shortest job first**, or SJF
- This is a non-preemptive, pre-emptive scheduling algorithm.
- Best approach to minimize waiting time.
- Easy to implement in Batch systems where required CPU time is known in advance.
- Impossible to implement where CPU time is unknown
- The processor should know in advance how much time process will take.

### Priority Based Scheduling

- Priority scheduling is a non-preemptive algorithm and one of the most common scheduling algorithm in batch systems.
- Each process is assigned a priority. Process with highest priority is executed first and so on.
- Processes with same priority are executed on FCFS basis.
- Priority can be decided based in memory requirements, time requirements or any other resource requirement.

### Shortest Remaining Time

- Shortest remaining time (SRT) is the preemptive version of the SJN algorithm.
- The processor is allocated to the job closest to completion but it can be preempted by a newer ready job with shorter time to completion.
- Impossible to implement in interactive systems where required CPU time is not known.
- It is often used in batch environments where short jobs need to give preference.

### Round Robin Scheduling

- Round Robin is the preemptive process scheduling algorithm.
- Each process is provided a fix time to execute, it is called a **quantum.**
- Once a process is executed for a given time period, it is preempted and other process executes for a given time period.
- Context Switching is used to save states of preempted processes.

### Multiple-Level Queues Scheduling

- Multiple queues are maintained for processes with common characteristics.
- Each queue can have its own scheduling algorithms.
- Priorities are assigned to each queue.
- For example, CPU-bound jobs can be scheduled in one queue and all I/O-bound jobs in another queue. The Process Scheduler then alternately selects jobs from each queue and assigns them to the CPU based on the algorithm assigned to the queue.