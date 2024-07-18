The comprehensive overview of kernel and user space components, their functions, and different types of kernels.

## Kernel
The kernel is the core component of an operating system, managing hardware interactions and performing essential tasks.

### Characteristics:
- **Heart/Core of OS**
- First part of OS to load on start-up

### Functions:
1. **Process Management:**
   - Scheduling processes and threads on CPUs
   - Creating and deleting user/system processes
   - Suspending and resuming processes
   - Providing mechanisms for process synchronization and communication

2. **Memory Management:**
   - Allocating and deallocating memory as needed
   - Tracking memory usage by processes

3. **File Management:**
   - Creating and deleting files and directories
   - Organizing files into directories
   - Mapping files to secondary storage
   - Providing backup support

4. **I/O Management:**
   - Managing I/O operations and devices
   - Buffering, caching, and spooling
     - **Spooling:** Managing tasks with differing speeds (e.g., print/mail spooling)
     - **Buffering:** Managing data transfer within a single job (e.g., video buffering)
     - **Caching:** Storing data for quick access (e.g., memory/web caching)

### Types of Kernels:
1. **Monolithic Kernel:**
   - All functions in the kernel
   - Bulky and requires high memory
   - Less reliable (one module crash affects the whole kernel)
   - High performance due to fast communication
   - Examples: Linux, Unix, MS-DOS

2. **Micro Kernel:**
   - Only major functions in the kernel (memory and process management)
   - File and I/O management in user space
   - Smaller, more reliable, and stable
   - Slower performance due to user-kernel mode switching overhead
   - Examples: L4 Linux, Symbian OS, MINIX

3. **Hybrid Kernel:**
   - Combines monolithic and microkernel advantages
   - File management in user space; rest in kernel space
   - Balanced speed and design with modularity and stability
   - Examples: MacOS, Windows NT/7/10

4. **Nano/Exo Kernels:**
   - Minimal kernel providing basic mechanisms, with most services in user space

## User Space
Where application software runs, without privileged access to hardware. Interacts with the kernel.

### Components:
- **GUI (Graphical User Interface)**
- **CLI (Command Line Interface)**

## Shell
A command interpreter that receives and executes user commands.

## Communication between User Mode and Kernel Mode
**Inter-Process Communication (IPC):**
1. Processes execute independently with separate memory (memory protection)
2. Communication via shared memory and message passing
