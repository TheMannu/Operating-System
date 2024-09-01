
# Process States and Queues

## 1. Process States
As a process executes, it transitions through several states. Each process can be in one of the following states:

- **New**: The operating system is about to pick the program and convert it into a process, or the process is being created.
- **Run**: The process is currently executing instructions with the CPU allocated to it.
- **Waiting**: The process is waiting for input/output (I/O) operations to complete.
- **Ready**: The process is in memory and ready to be assigned to a processor but is not currently executing.
- **Terminated**: The process has finished its execution, and its Process Control Block (PCB) entry is removed from the process table.

## 2. Process Queues
Different queues manage processes in various states:

- **Job Queue**:
  - Contains processes in the New state.
  - Processes in this queue are present in secondary memory.
  - The Job Scheduler (Long-term Scheduler or LTS) selects processes from this pool and loads them into memory for execution.

- **Ready Queue**:
  - Contains processes in the Ready state.
  - Processes in this queue reside in the main memory.
  - The CPU Scheduler (Short-term Scheduler) picks processes from the Ready Queue and dispatches them to the CPU for execution.

- **Waiting Queue**:
  - Contains processes in the Waiting state.

## 3. Degree of Multiprogramming
The degree of multiprogramming refers to the number of processes present in memory simultaneously. The Long-term Scheduler (LTS) controls the degree of multiprogramming.

## 4. Dispatcher
The dispatcher is a module within the operating system that gives control of the CPU to the process selected by the Short-term Scheduler (STS).
