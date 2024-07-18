## How Apps Interact with the Kernel Using System Calls

### Basics of System Calls
- System calls are the mechanism through which a user program requests services from the kernel.
- They are essential because user programs typically lack permissions for operations like I/O device access and inter-process communication.
- System calls transition a process from user mode to kernel mode using software interrupts.
- They are implemented in C and are the only way for a process to execute privileged operations.

### Example: `mkdir` System Call
- `mkdir` command indirectly calls the kernel's file management module to create a new directory.
- It acts as a wrapper around the actual system call responsible for directory creation.
- `mkdir` interacts with the kernel by making a system call.

### Example: Creating a Process
- User executes a process in user space.
- The process issues a system call to request kernel services.
- The kernel executes the requested operation (e.g., process creation).
- Control returns to the user space after the kernel operation completes.

### Types of System Calls
1. **Process Control**
   - `end`, `abort`
   - `load`, `execute`
   - `create process`, `terminate process`
   - `get process attributes`, `set process attributes`
   - `wait for time`
   - `wait event`, `signal event`
   - `allocate` and `free memory`

2. **File Management**
   - `create file`, `delete file`
   - `open`, `close`
   - `read`, `write`, `reposition`
   - `get file attributes`, `set file attributes`

3. **Device Management**
   - `request device`, `release device`
   - `read`, `write`, `reposition`
   - `get device attributes`, `set device attributes`
   - `logically attach` or `detach devices`

4. **Information Maintenance**
   - `get time` or `date`, `set time` or `date`
   - `get system data`, `set system data`
   - `get process`, `file`, or `device attributes`
   - `set process`, `file`, or `device attributes`

5. **Communication Management**
   - `create`, `delete communication connection`
   - `send`, `receive messages`
   - `transfer status information`
   - `attach` or `detach remote devices`

### Examples of System Calls in Windows and Unix
| Category | Windows System Calls         | Unix System Calls        |
|----------|------------------------------|--------------------------|
| Process Control | `CreateProcess()`       | `fork()`                 |
|              | `ExitProcess()`         | `exit()`                 |
|              | `WaitForSingleObject()` | `wait()`                 |
| File Management | `CreateFile()`          | `open()`                 |
|              | `ReadFile()`            | `read()`                 |
|              | `WriteFile()`           | `write()`                |
|              | `CloseHandle()`         | `close()`                |
|              | `SetFileSecurity()`     | `chmod()`, `chown()`     |
| Device Management | `SetConsoleMode()`  | `ioctl()`                |
|              | `ReadConsole()`         | `read()`, `write()`       |
| Information Management | `GetCurrentProcessID()` | `getpid()`               |
|              | `SetTimer()`            | `alarm()`, `sleep()`      |
| Communication Management | `CreatePipe()`      | `pipe()`                 |
|              | `CreateFileMapping()`   | `shmget()`, `mmap()`      |

