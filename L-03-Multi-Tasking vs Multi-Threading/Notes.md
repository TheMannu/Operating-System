
# Multi-Tasking vs Multi-Threading

**Program**
- An executable file containing a set of instructions written to complete a specific job or operation on your computer.
- It is compiled code, ready to be executed.
- Stored on the disk.

**Process** - A program under execution. Resides in the computer's primary memory (RAM).

**Thread**
- A single sequence stream within a process.
- An independent path of execution in a process.
- Also known as a light-weight process.
- Used to achieve parallelism by dividing a process's tasks into multiple independent paths of execution.
- Example: In a text editor, typing, spell-checking, formatting of text, and saving the text are done using multiple threads.

**Multi-Tasking**
- The execution of more than one task simultaneously is called multitasking.
- Involves the concept of more than one process being context switched.
- Number of CPUs can be 1.
- Isolation and memory protection exits.
- The OS must allocate separate memory and resources to each program that CPU is executing.

**Multi-Threading**
- When a process is divided into several different sub-tasks called threads, each with its own path of execution. Concept is called multithreading
- Concept of more then 1 thread.Threads are context switched.
- Number of CPUs >= 1 (better to have more than 1).
- No isolation and memory protection; resources are shared among threads of the same process.
- The OS allocates memory to a process, and multiple threads of that process share the same memory and resources allocated to the process.

## Thread Scheduling
- Threads are scheduled for execution based on their priority.
- Even though threads execute within the runtime, all threads are assigned processor time slices by the operating system.

**Difference between Thread Context Switching and Process Context Switching:**

**Thread Context Switching**
- The OS saves the current state of a thread and switches to another thread within the same process.
- Does not include switching of memory address space.(But Program counter, registers & stack are
included.)
- Involves switching the program counter, registers, and stack.
- Fast switching because the CPU's cache state is preserved.

**Process Context Switching**
- The OS saves the current state of a process and switches to another process by restoring its state.
- Includes switching of memory address space.
- Slower switching because the CPU's cache state is flushed.

