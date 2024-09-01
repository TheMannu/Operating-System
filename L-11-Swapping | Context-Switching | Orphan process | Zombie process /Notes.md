
# Process Management Concepts

## 1. Swapping
- **Medium-Term Scheduling (MTS):** 
  - In a time-sharing system, MTS may be present to manage processes.
- **Reducing Multi-Programming:** 
  - Processes may be removed from memory to reduce the degree of multi-programming.
- **Reintroduction of Processes:** 
  - Removed processes can be reintroduced into memory and continue execution from where they left off; this is known as swapping.
- **Swap Operations:** 
  - Swap-out and swap-in operations are handled by MTS.
- **Purpose of Swapping:** 
  - Swapping improves process mix or frees up memory when overcommitted.

## 2. Context-Switching
- **CPU Switching:**
  - Switching the CPU to another process involves saving the current process's state and restoring the state of the next process.
- **State Management:**
  - The kernel saves the context of the old process in its Process Control Block (PCB) and loads the saved context of the new process.
- **Overhead:**
  - Context-switching is considered pure overhead as no useful work is done during the switch.
- **Speed Variation:**
  - The speed of context-switching varies depending on factors like memory speed and the number of registers to be copied.

## 3. Orphan Process
- **Definition:**
  - An orphan process is a process whose parent has terminated but the process is still running.
- **Adoption by Init:**
  - Orphan processes are adopted by the `init` process, which is the first process of the operating system.

## 4. Zombie Process / Defunct Process
- **Definition:**
  - A zombie process is a process that has completed execution but still has an entry in the process table.
- **Occurrence:**
  - Zombie processes usually occur for child processes as the parent process still needs to read the child’s exit status.
- **Reaping Zombie Process:**
  - Once the parent process reads the exit status using the `wait` system call, the zombie process is removed from the process table.
- **Reason for Persistence:**
  - The child process remains a zombie until the parent process reads its exit status and it is removed from the process table.
