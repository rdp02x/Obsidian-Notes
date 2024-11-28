### What is Scheduling?
- **Scheduling** is a method to allocate computing resources like processor time, memory, and bandwidth to different processes, threads, and applications.
- The goal is to balance the system load, ensure resources are distributed evenly, and prioritize tasks based on specific rules.
- Scheduling is also known as **process scheduling**.

### Process Scheduling
- **Process Scheduling** is the activity of the process manager that involves switching the CPU between different processes.
- This function is part of the operating system's job to manage processes in various states (e.g., scheduling, running, waiting).
- It is crucial in multiprogramming and multitasking environments where multiple processes run at the same time.
- Scheduling ensures that the CPU is used efficiently by having processes run at specific times.

### Process Scheduling Queues
- The OS uses **Process Scheduling Queues** to manage PCBs (Process Control Blocks).
- When a process's state changes, its PCB is moved to the appropriate queue.
- Types of queues include:
  1. **Job Queue:** Contains all processes in the system.
  2. **Ready Queue:** Holds processes in main memory, ready to execute.
  3. **Device Queue:** Contains processes waiting for I/O devices.

### Schedulers
- **Schedulers** are system software that manage the scheduling of processes.
- There are three types of schedulers:
  1. **Long-Term Scheduler (Job Scheduler):** Decides which processes are admitted to the system and placed in the ready queue.
  2. **Mid-Term Scheduler:** Manages swapping processes in and out of memory to control the level of multiprogramming.
  3. **Short-Term Scheduler (CPU Scheduler):** Determines which process from the ready queue gets CPU time and moves processes to the running state.

### Context Switching
- **Context Switching** involves saving and restoring the state of a process so it can resume execution later.
- It is essential for multitasking, allowing a single CPU to handle multiple processes by switching between them.
- During a context switch, the state of the current process is saved, and the state of the next process is loaded from its Process Control Block (PCB).

### Scheduling Algorithms

- **Purpose:** The process scheduler uses scheduling algorithms to decide which processes get to use the CPU and for how long.

- **Types of Scheduling Algorithms:**
  1. **Non-Preemptive Algorithms:**
     - Once a process starts running, it cannot be stopped until it finishes its allocated time or completes its execution.
     - The running process keeps the CPU until it is done, even if a higher-priority process arrives.

  2. **Preemptive Algorithms:**
     - The scheduler can interrupt a currently running process if a higher-priority process arrives.
     - This allows the CPU to be given to more important or time-sensitive tasks as needed.

### First Come First Serve (FCFS)

**Overview:**
- Jobs are executed in the order they arrive.
- Simple to understand and implement.
- Uses a FIFO (First In, First Out) queue.
- Performance can be poor due to high average waiting time.

**Example:**

Consider the following set of processes with their arrival and burst times:

| Process | Arrival Time | Burst Time |
|---------|--------------|------------|
| P1      | 0            | 4          |
| P2      | 1            | 3          |
| P3      | 2            | 1          |
| P4      | 3            | 2          |
| P5      | 4            | 5          |

**Gantt Chart:**

```
P1      P2      P3  P4   P5
0       4       7   8    15
```

**Calculation of Waiting Time and Turnaround Time:**

| Process | Arrival Time | Burst Time | Waiting Time | Turnaround Time |
|---------|--------------|------------|--------------|-----------------|
| P1      | 0            | 4          | 0            | 4               |
| P2      | 1            | 3          | 3            | 6               |
| P3      | 2            | 1          | 5            | 6               |
| P4      | 3            | 2          | 5            | 7               |
| P5      | 4            | 5          | 6            | 11              |

**Formulas:**
- **Waiting Time** = Turnaround Time - Burst Time
- **Turnaround Time** = Finish Time - Arrival Time

**Summary:**

- **Total Waiting Time** = 0 + 3 + 5 + 5 + 6 = 19 ms
- **Average Waiting Time** = 19 ms / 5 = 3.8 ms
- **Total Turnaround Time** = 4 + 6 + 6 + 7 + 11 = 34 ms
- **Average Turnaround Time** = 34 ms / 5 = 6.8 ms

### Shortest Job First (SJF)

**Overview:**
- Also known as Shortest Job First or SJF.
- Aims to minimize waiting time.
- Ideal for batch systems where CPU time is known in advance.
- Not suitable for interactive systems where CPU time is unpredictable.
- Requires knowledge of the process's burst time beforehand.

**Example:**

Consider the following set of processes with their arrival and burst times:

| Process | Arrival Time | Burst Time |
|---------|--------------|------------|
| P1      | 0            | 4          |
| P2      | 1            | 3          |
| P3      | 2            | 1          |
| P4      | 3            | 2          |
| P5      | 4            | 6          |

**Gantt Chart:**

```
P1      P3  P4   P2      P5
0       4   5    7       16
```

**Calculation of Waiting Time and Turnaround Time:**

| Process | Arrival Time | Burst Time | Waiting Time | Turnaround Time |
|---------|--------------|------------|--------------|-----------------|
| P1      | 0            | 4          | 0            | 4               |
| P2      | 1            | 3          | 6            | 9               |
| P3      | 2            | 1          | 2            | 3               |
| P4      | 3            | 2          | 2            | 4               |
| P5      | 4            | 6          | 6            | 12              |

**Formulas:**
- **Waiting Time** = Turnaround Time - Burst Time
- **Turnaround Time** = Finish Time - Arrival Time

**Summary:**

- **Total Waiting Time** = 0 + 6 + 2 + 2 + 6 = 16 ms
- **Average Waiting Time** = 16 ms / 5 = 3.2 ms
- **Total Turnaround Time** = 4 + 9 + 3 + 4 + 12 = 32 ms
- **Average Turnaround Time** = 32 ms / 5 = 6.4 ms

### Priority Scheduling

**Overview:**
- Each process is assigned a priority.
- The process with the highest priority is executed first.
- Processes with the same priority are executed in a First Come, First Serve (FCFS) manner.
- Priority can be based on memory needs, time requirements, or other resources.

**Example:**

Consider the following set of processes with their arrival times, burst times, and priorities:

| Process | Arrival Time | Burst Time | Priority |
|---------|--------------|------------|----------|
| P1      | 0            | 4          | 4        |
| P2      | 1            | 5          | 5        |
| P3      | 2            | 1          | 7        |
| P4      | 3            | 2          | 2        |
| P5      | 4            | 3          | 1        |
| P6      | 5            | 6          | 6        |

**Gantt Chart:**

```
P1      P3   P6    P2   P4   P5
0       4    5     11   16   18
```

**Calculation of Waiting Time and Turnaround Time:**

| Process | Arrival Time | Burst Time | Turnaround Time | Waiting Time |
|---------|--------------|------------|-----------------|--------------|
| P1      | 0            | 4          | 4               | 0            |
| P2      | 1            | 5          | 15              | 10           |
| P3      | 2            | 1          | 3               | 2            |
| P4      | 3            | 2          | 15              | 13           |
| P5      | 4            | 3          | 17              | 14           |
| P6      | 5            | 6          | 6               | 0            |

**Formulas:**
- **Turnaround Time** = Finish Time - Arrival Time
- **Waiting Time** = Turnaround Time - Burst Time

**Summary:**

- **Total Waiting Time** = 0 + 10 + 2 + 13 + 14 + 0 = 39 ms
- **Average Waiting Time** = 39 ms / 6 = 6.5 ms
- **Total Turnaround Time** = 4 + 15 + 3 + 15 + 17 + 6 = 60 ms
- **Average Turnaround Time** = 60 ms / 6 = 10 ms


### Round Robin (RR)

**Overview:**
- Also known as time slicing.
- Each process is given a fixed time slice (quantum) in advance.
- A clock interrupt is generated at periodic intervals.
- When an interrupt occurs, the currently running process is placed in the ready queue.
- The next ready job is selected for execution.

**Example:**

Consider the following set of processes with their arrival times and burst times:

| Process | Arrival Time | Burst Time |
|---------|--------------|------------|
| P1      | 0            | 8          |
| P2      | 1            | 4          |
| P3      | 2            | 9          |
| P4      | 3            | 5          |

**Time Quantum:** 4 units

**Gantt Chart:**

```
P1      P2    P3    P4    P1    P3    P4    P3
0       4     8     12    16    20    24    25
```

**Calculation of Waiting Time and Turnaround Time:**

| Process | Arrival Time | Burst Time | Waiting Time | Turnaround Time |
|---------|--------------|------------|--------------|-----------------|
| P1      | 0            | 8          | 20           | 12              |
| P2      | 1            | 4          | 7            | 3               |
| P3      | 2            | 9          | 24           | 15              |
| P4      | 3            | 5          | 22           | 17              |

**Formulas:**
- **Turnaround Time** = Finish Time - Arrival Time
- **Waiting Time** = Turnaround Time - Burst Time

**Summary:**

- **Total Waiting Time** = 20 + 7 + 24 + 22 = 47 ms
- **Average Waiting Time** = 47 ms / 4 = 11.75 ms
- **Total Turnaround Time** = 12 + 3 + 15 + 17 = 47 ms
- **Average Turnaround Time** = 47 ms / 4 = 11.75 ms

### Multiprocessor Scheduling

**Overview:**
In a multiprocessor system, the scheduler must determine which process to run and which CPU to assign it to.

1. **Timesharing:**
   - A common approach is to use a system-wide data structure for managing ready processes.
   - This could be a single list or a set of lists categorized by process priority.
   - Suitable for managing unrelated processes across multiple CPUs.

2. **Space Sharing:**
   - Involves scheduling related processes or threads simultaneously across multiple CPUs.
   - Reduces context switching overhead by eliminating multiprogramming for related processes.

3. **Gang Scheduling:**
   - **Groups of Related Threads:** Threads that work together are scheduled as a unit.
   - **Simultaneous Execution:** All threads in the group run simultaneously on different CPUs.
   - **Coordinated Timing:** All members of the gang start and finish their time slices together.

### Real-Time Scheduling

**Overview:**
Real-time systems must respond within a specified time frame, meeting deadlines to avoid failure in critical applications.

1. **Hard Real-Time System:**
   - **Deadline Compliance:** Must never miss a deadline. Missing a deadline can have severe consequences.
   - **Example:** Flight control systems.

2. **Soft Real-Time System:**
   - **Deadline Tolerance:** Can occasionally miss deadlines with an acceptably low probability.
   - **Usefulness Decreases:** The value of results diminishes with increased tardiness.
   - **Example:** Telephone switches.

**Reference Model of Real-Time Scheduling:**
- **Workload Model:** Defines the application supported by the system.
- **Resource Model:** Specifies available resources for the application.
- **Algorithms:** Detail how resources are allocated and used by the application.

**Real-Time Scheduling Terms:**

| Term                   | Description |
|------------------------|-------------|
| **Job**                | A unit of work that may require resources and can be allocated to a processor. |
| **Task**               | A set of related jobs providing specific system functionality. |
| **Release Time**       | Time at which a job becomes ready for execution. |
| **Execution Time**     | Time taken to execute a job. |
| **Deadline**           | Time by which a job must be completed. Deadlines can be absolute or relative. |
| **Response Time**      | Time from job release to completion. |
