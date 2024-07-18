# Operating System Components

## Kernel

A kernel is the part of the operating system that interacts directly with the hardware and performs the most crucial tasks.

### Characteristics:
- **Heart/Core of OS**
- First part of OS to load on start-up

### Functions:
1. **Process Management:**
   - Scheduling processes and threads on CPUs
   - Creating and deleting both user and system processes
   - Suspending and resuming processes
   - Providing mechanisms for process synchronization and communication

2. **Memory Management:**
   - Allocating and deallocating memory space as needed
   - Keeping track of memory usage by processes

3. **File Management:**
   - Creating and deleting files
   - Creating and deleting directories to organize files
   - Mapping files into secondary storage
   - Providing backup support onto a stable storage media

4. **I/O Management:**
   - Managing and controlling I/O operations and devices
   - Buffering, caching, and spooling
     - **Spooling:**
       - Managing tasks with differing speeds (e.g., print spooling and mail spooling)
     - **Buffering:**
       - Managing data transfer within a single job (e.g., YouTube video buffering)
     - **Caching:**
       - Storing data for quick access (e.g., memory caching, web caching)
   
### Types of Kernels:
1. **Monolithic Kernel:**
   - All functions are in the kernel itself
   - Bulky in size
   - High memory requirement
   - Less reliable (one module crash affects the whole kernel)
   - High performance due to fast communication
   - Examples: Linux, Unix, MS-DOS

2. **Micro Kernel:**
   - Only major functions are in the kernel
     - Memory management
     - Process management
   - File management and I/O management are in user space
   - Smaller in size
   - More reliable and stable
   - Slower performance due to overhead of switching between user mode and kernel mode
   - Examples: L4 Linux, Symbian OS, MINIX

3. **Hybrid Kernel:**
   - Combines advantages of both monolithic and micro kernels
   - File management in user space; rest in kernel space
   - Balanced speed and design with modularity and stability
   - Examples: MacOS, Windows NT/7/10

4. **Nano/Exo Kernels:**
   - Minimal kernel providing basic mechanisms, with most services in user space

## User Space

The user space is where application software runs, without privileged access to the underlying hardware. It interacts with the kernel.

### Components:
- **GUI (Graphical User Interface)**
- **CLI (Command Line Interface)**

## Shell

A shell, also known as a command interpreter, is the part of the operating system that receives commands from the users and executes them.

## Communication between User Mode and Kernel Mode

**Inter-Process Communication (IPC):**
1. Two processes execute independently, having independent memory space (memory protection). However, some processes may need to communicate to work.
2. Communication is done by shared memory and message passing.
