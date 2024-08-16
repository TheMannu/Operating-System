# Lec-9: Introduction to Process

1. **What is a program?**
   - A program is a compiled code that is ready to execute.

2. **What is a process?**
   - A process is a program under execution.

3. **How does the OS create a process?**
   - The OS creates a process by converting a program into a process.
   
   **Steps:**
   a. Load the program and static data into memory.
   b. Allocate runtime stack.
   c. Allocate heap memory.
   d. Perform I/O tasks.
   e. OS hands off control to `main()`.

4. **Architecture of a process:**
   - **Stack:** Contains local variables, function arguments, and return values.
   - **Heap:** Contains dynamically allocated variables.
   - **Data:** Contains global and static data.
   - **Text:** Contains compiled code (loaded from disk).

5. **Attributes of a process:**
   a. Feature that allows identifying a process uniquely.
   b. **Process table:**
      - All processes are being tracked by the OS using a table-like data structure.
      - Each entry in that table is a Process Control Block (PCB).
   c. **PCB (Process Control Block):**
      - Stores information/attributes of a process.
      - Data structure used for each process, that stores information such as process ID, program counter, process state, priority, etc.

6. **PCB Structure:**
   - **Process ID:** Unique identifier of the process.
   - **Program Counter (PC):** Next instruction address of the program.
   - **Process State:** Current state of the process.
   - **Priority:** Based on priority, a process gets CPU time.
   - **Registers:** Stores the current values of process-specific registers. When a process is running and its time slice expires, the current value of the registers is stored in the PCB, and the process is swapped out. When the process is scheduled to run again, the register values are read from the PCB and written to the CPU registers.
   - **List of open files:** Files that the process has opened.
   - **List of open devices:** Devices that the process has opened.
   - **Unique identifier:** Ensures the uniqueness of the process within the system.
