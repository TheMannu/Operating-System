### Program
- **Definition**: An executable file containing a set of instructions to complete a specific job or operation on a computer.
- **Characteristics**:
  - **Compiled Code**: The code is pre-processed into machine language, making it ready to be executed by the computer's CPU.
  - **Storage**: It is stored on the computer's disk (e.g., hard drive, SSD).

### Process
- **Definition**: A program under execution.
- **Characteristics**:
  - **Execution State**: When a program is running, it becomes a process.
  - **Memory Location**: It resides in the computer's primary memory (RAM).

### Thread
- **Definition**: A single sequence stream within a process.
- **Characteristics**:
  - **Independent Execution Path**: Threads allow multiple sequences of instructions to be executed within the same process.
  - **Light-weight Process**: Threads share the same memory and resources of the process but operate independently.
  - **Parallelism**: Achieves parallelism by dividing a process's tasks into multiple independent paths of execution.
  - **Example**: In a text editor, different threads might handle typing, spell-checking, formatting, and saving text simultaneously.

### Multi-Tasking
- **Definition**: The execution of more than one task simultaneously.
- **Characteristics**:
  - **Multiple Processes**: Involves the concept of more than one process being context switched.
  - **CPU Utilization**: Can be done even with a single CPU by quickly switching between processes.
  - **Isolation and Memory Protection**: Each process operates in its own memory space, ensuring isolation and protection.
  - **Resource Allocation**: The OS allocates separate memory and resources to each program.

### Multi-Threading
- **Definition**: When a process is divided into several different sub-tasks called threads, each with its own path of execution.
- **Characteristics**:
  - **Multiple Threads**: Involves more than one thread within a single process.
  - **Context Switching**: Threads are context switched, meaning the CPU switches between threads to give the illusion of parallelism.
  - **CPU Utilization**: Works efficiently with multiple CPUs but can also be implemented on a single CPU.
  - **Shared Resources**: Threads share the same memory and resources of the process, lacking isolation and memory protection.
  - **OS Memory Allocation**: The OS allocates memory to the entire process, and multiple threads within that process share this memory.

### Thread Scheduling
- **Execution Priority**: Threads are scheduled for execution based on their priority.
- **Processor Time Slices**: The operating system assigns processor time slices to threads, allowing them to execute in turn.

### Difference Between Thread Context Switching and Process Context Switching

#### Thread Context Switching
- **State Saving**: The OS saves the current state of a thread and switches to another thread within the same process.
- **Memory Address Space**: Does not include switching of memory address space.
- **Components Involved**: Program counter, registers, and stack are switched.
- **Speed**: Fast switching because the CPU's cache state is preserved, reducing overhead.

#### Process Context Switching
- **State Saving**: The OS saves the current state of a process and switches to another process by restoring its state.
- **Memory Address Space**: Includes switching of memory address space.
- **Speed**: Slower switching because the CPU's cache state is flushed, increasing overhead.

### Summary
- **Programs** are static, executable files stored on disk.
- **Processes** are dynamic executions of programs residing in RAM.
- **Threads** are smaller execution units within processes, allowing parallelism and more efficient CPU usage.
- **Multi-Tasking** involves running multiple processes, each isolated with its own memory space.
- **Multi-Threading** involves running multiple threads within a single process, sharing the same memory and resources.
- **Thread Scheduling** and **Context Switching** are crucial for managing how threads and processes use CPU time and system resources efficiently.
