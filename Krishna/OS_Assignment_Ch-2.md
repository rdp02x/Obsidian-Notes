### 1. Difference Between Program and Process
- **Program:**
  - A static set of instructions stored in a file.
  - Passive entity, which does not perform any action until executed.
  - Exists on disk as an executable file.
  - Example: A Python script or an application.

- **Process:**
  - A program in execution, which is active and dynamic.
  - A process has a lifecycle that involves states like ready, running, waiting, etc.
  - Exists in memory (RAM) and consumes system resources.
  - Example: When you run a Python script, it becomes a process.

### 2. Explain Process Life Cycle
The process life cycle refers to the stages a process goes through from creation to termination:
- **New:** The process is being created.
- **Ready:** The process is waiting to be assigned to a CPU.
- **Running:** The process is currently being executed by the CPU.
- **Waiting (Blocked):** The process is waiting for some event (like I/O completion).
- **Terminated:** The process has finished execution.

### 3. Explain Process Control Block (PCB)
- **Process Control Block (PCB):** A data structure in the operating system that stores information about a process.
- **Components of PCB:**
  - **Process ID:** Unique identifier for the process.
  - **Process State:** Current state (new, ready, running, waiting, terminated).
  - **Program Counter:** The address of the next instruction to execute.
  - **CPU Registers:** Values of CPU registers.
  - **Memory Management Information:** Information about memory allocated to the process.
  - **I/O Status Information:** List of I/O devices allocated to the process.
  - **Accounting Information:** CPU usage, time limits, etc.

### 4. Difference Between Preemptive and Non-Preemptive Scheduling
- **Preemptive Scheduling:**
  - CPU can be taken away from a process if a higher-priority process arrives.
  - Ensures better response times and is more flexible.
  - Example: Round Robin, Priority Scheduling.

- **Non-Preemptive Scheduling:**
  - Once the CPU is assigned to a process, it cannot be taken away until the process completes or voluntarily relinquishes it.
  - Simpler to implement but can lead to poor system performance.
  - Example: First-Come, First-Served (FCFS), Shortest Job Next (SJN).

### 5. Define Terms Scheduling, Scheduler, and Scheduling Algorithm
- **Scheduling:** The process of deciding which process will get access to the CPU and for how long.
- **Scheduler:** The component of the OS responsible for managing the scheduling of processes.
  - **Types of Schedulers:**
    - **Long-term Scheduler:** Decides which processes are admitted to the ready queue.
    - **Short-term Scheduler:** Decides which of the ready processes gets the CPU next.
    - **Medium-term Scheduler:** Handles swapping processes in and out of memory.
- **Scheduling Algorithm:** A method used by the scheduler to determine the order of process execution (e.g., FCFS, SJF, Round Robin).

### 6. Differentiate Long-term Scheduler, Medium-term Scheduler, and Short-term Scheduler
- **Long-term Scheduler (Job Scheduler):**
  - Decides which processes to add to the pool of processes that are ready to execute.
  - Controls the degree of multiprogramming.
  - Invoked infrequently.

- **Medium-term Scheduler:**
  - Temporarily removes processes from memory (swapping) to reduce multiprogramming and then reintroduces them later.
  - Helps manage memory and improve process performance.

- **Short-term Scheduler (CPU Scheduler):**
  - Decides which of the ready, in-memory processes is executed next by the CPU.
  - Invoked frequently, typically every few milliseconds.

### 7. Define the Following Terms:
- **CPU Utilization:** The percentage of time the CPU is actively working on processes.
- **Throughput:** The number of processes completed in a given amount of time.
- **Turn-around Time:** The total time taken from submission of a process to its completion.
- **Waiting Time:** The total time a process spends in the ready queue waiting for CPU time.
- **Response Time:** The time from the submission of a request until the first response is produced.
- **Quantum:** The fixed time allocated to each process in Round Robin scheduling.
- **Mutual Exclusion:** A principle stating that only one process can access a critical section of code at a time to prevent race conditions.

### 8. List of Scheduling Algorithms
- First-Come, First-Served (FCFS)
- Shortest Job First (SJF) or Shortest Job Next (SJN)
- Priority Scheduling
- Round Robin (RR)
- Multilevel Queue Scheduling
- Multilevel Feedback Queue Scheduling

### 9. Explain FCFS (First Come First Served) with Example
- **FCFS Algorithm:** The simplest scheduling algorithm where the process that arrives first is executed first.
- **Example:**
  - Processes: P1 (burst time 4), P2 (burst time 3), P3 (burst time 5)
  - Order of Execution: P1 -> P2 -> P3

  **Gantt Chart:**
  ```
  | P1 | P2 | P3 |
  0    4    7   12
  ```

  **Turn-around Times:** P1: 4, P2: 7, P3: 12  
  **Average Turn-around Time:** (4 + 7 + 12) / 3 = 7.67  
  **Waiting Times:** P1: 0, P2: 4, P3: 7  
  **Average Waiting Time:** (0 + 4 + 7) / 3 = 3.67

### 10. Explain SJF/SPN Algorithm with Example
- **SJF Algorithm (Shortest Job First):** Schedules the process with the smallest execution time next.
- **Example:**
  - Processes: P1 (burst time 8), P2 (burst time 4), P3 (burst time 9), P4 (burst time 5)
  - Order of Execution: P2 -> P4 -> P1 -> P3

  **Gantt Chart:**
  ```
  | P2 | P4 | P1 | P3 |
  0    4    9   17   26
  ```

  **Turn-around Times:** P2: 4, P4: 9, P1: 17, P3: 26  
  **Average Turn-around Time:** (4 + 9 + 17 + 26) / 4 = 14  
  **Waiting Times:** P2: 0, P4: 4, P1: 9, P3: 17  
  **Average Waiting Time:** (0 + 4 + 9 + 17) / 4 = 7.5

### 11. Explain Round Robin Algorithm with Example
- **Round Robin (RR) Algorithm:** Each process is assigned a fixed time (quantum) in a cyclic order.
- **Example:**
  - Processes: P1 (burst time 10), P2 (burst time 4), P3 (burst time 5)
  - Quantum: 3

  **Gantt Chart:**
  ```
  | P1 | P2 | P3 | P1 | P3 | P1 |
  0    3    6    9   12   15   17
  ```

  **Turn-around Times:** P1: 17, P2: 6, P3: 15  
  **Average Turn-around Time:** (17 + 6 + 15) / 3 = 12.67  
  **Waiting Times:** P1: 7, P2: 2, P3: 9  
  **Average Waiting Time:** (7 + 2 + 9) / 3 = 6

### 12. Explain Race Condition with Example
- **Race Condition:** Occurs when two or more processes access shared resources simultaneously, leading to unpredictable results.
- **Example:**
  - Two processes trying to update a shared variable concurrently can lead to inconsistent data if proper synchronization is not used.

### 13. Explain Deadlock in Detail
- **Deadlock:** A situation where a set of processes are blocked because each process is holding a resource and waiting for another resource that is being held by another process in the set.
- **Necessary Conditions for Deadlock:**
  - **Mutual Exclusion:** Only one process can use a resource at a time.
  - **Hold and Wait:** A process holding a resource is waiting for additional resources.
  - **No Preemption:** Resources cannot be forcibly taken from a process.
  - **Circular Wait:** A set of processes are waiting for each other in a circular chain.

- **Deadlock Prevention, Avoidance, and Detection:** Techniques like resource allocation graphs, Banker's algorithm, or implementing timeouts can help prevent or handle deadlocks.

### 14. Calculate Average Turn-around Time & Average Waiting Time for All Algorithms with Gantt Chart for Given Data
**Given Data:**

| Process | Arrival Time | Execution Time |
|---------|--------------|----------------|
| P0      | 0            | 5              |
| P1      | 1            | 3              |
| P2      | 2            | 8              |
| P3      | 3            | 6              |

**FCFS:**
- **Gantt Chart:**
  ```
  | P0 | P1 | P2 | P3 |
  0    5    8   16   22
  ```

- **Turn-around Times:** P0: 5, P1: 7, P2: 14, P3: 19  
- **Average Turn-around Time:** (5 + 7 + 14 + 19) / 4 = 11.25  
- **Waiting Times:** P0: 0, P1: 4, P2: 8, P3: 13  
- **Average Waiting Time:** (0 + 4 + 8 + 13) / 4 = 6.25

#### SJF (Shortest Job First):
- **Gantt Chart:**
  ```
  | P1 | P0 | P3 | P2 |
  1    4    9   15   23
  ```

- **Turn-around Times:** P1: 3, P0: 5, P3: 12, P2: 21  
- **Average Turn-around Time:** (3 + 5 + 12 + 21) / 4 = 10.25  
- **Waiting Times:** P1: 0, P0: 1, P3: 6, P2: 13  
- **Average Waiting Time:** (0 + 1 + 6 + 13) / 4 = 5

#### Round Robin (Quantum = 4):
- **Gantt Chart:**
  ```
  | P0 | P1 | P2 | P3 | P2 |
  0    4    7   11   15   19   22
  ```

- **Turn-around Times:** P0: 9, P1: 6, P2: 20, P3: 19  
- **Average Turn-around Time:** (9 + 6 + 20 + 19) / 4 = 13.5  
- **Waiting Times:** P0: 4, P1: 3, P2: 12, P3: 13  
- **Average Waiting Time:** (4 + 3 + 12 + 13) / 4 = 8.25
