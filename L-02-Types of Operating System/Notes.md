
# Operating Systems (OS)

## Goals of an Operating System
- **Maximum CPU utilization**
- **Less process starvation**
- **Higher priority job execution**

## Types of Operating Systems
1. **Single Process Operating System**
2. **Batch-Processing Operating System**
3. **Multiprogramming Operating System**
4. **Multitasking Operating System**
5. **Multiprocessing Operating System**
6. **Distributed System**
7. **Real-Time OS**

## Examples of Operating Systems and Their Types
- **MS-DOS (1981)**: Single process system
- **ATLAS (Manchester University, late 1950s - early 1960s)**: Batch-processing system
- **THE (Dijkstra, early 1960s)**: Multiprogramming operating system
- **CTS (MIT, early 1960s)**: Multitasking system
- **Windows NT**: Multiprocessing system
- **LOCUS**: Distributed operating system
- **ATCSJ**: Real-time OS

# Types of Operating Systems

## Single Process OS
- Only 1 process executes at a time from the ready queue.

## Old Batch-processing OS
1. User prepares his job using punch cards.
2. User submits the job to the computer operator.
3. Operator collects the jobs from different users and sorts the jobs into batches with similar needs.
4. Operator submits the batches to the processor one by one.
5. All the jobs of one batch are executed together.

### Characteristics:
- Priorities cannot be set; if a job comes with higher priority.
- May lead to starvation (A batch may take more time to complete).
- CPU may become idle in case of I/O operations.

## Multiprogramming OS
- Increases CPU utilization by keeping multiple jobs (code and data) in the memory so that the CPU always has one to execute in case some job gets busy with I/O operations.
- Single CPU.
- Context switching for processes.
- Switch happens when current process goes to wait state.
- CPU idle time reduced.

## Multitasking OS
- A logical extension of multiprogramming.
- Single CPU.
- Able to run more than one task simultaneously.
- Context switching and time sharing used.
- Increases responsiveness.
- CPU idle time is further reduced.

## Multi-processing OS
- More than 1 CPU in a single computer.
- Increases reliability; if 1 CPU fails, others can work.
- Better throughput.
- Lesser process starvation (if 1 CPU is working on some process, another can be executed on another CPU).

## Distributed OS
- OS manages many bunches of resources like CPUs, memory, GPUs, etc.
- Loosely connected autonomous, interconnected computer nodes.
- Collection of independent, networked, communicating, and physically separate computational nodes.

## Real-Time OS (RTOS)
- Real-time error-free computations within tight time boundaries.
- Used in applications such as air traffic control systems, robots, etc.

