
### How Apps Interact with Kernel Using System Calls

#### Basics of System Calls
- System calls are mechanisms through which user programs request services from the kernel.
- They allow processes to execute privileged operations like I/O device access and inter-process communication.
- Implemented in C, system calls transition a process from user mode to kernel mode using software interrupts.

#### Example: `mkdir` System Call
- `mkdir` indirectly calls the kernel's file management module to create a directory.
- It acts as a wrapper around the actual system call for directory creation.
- `mkdir` interacts with the kernel using system calls.

#### Example: Creating a Process
- User space: User executes a process.
- User space to Kernel space: Process issues a system call to create a new process.
- Kernel space: Executes requested operation (e.g., process creation).
- Kernel space to User space: Control returns after operation completes.

#### Types of System Calls
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

#### Examples of System Calls in Windows and Unix
| Category               | Windows System Calls           | Unix System Calls           |
|------------------------|--------------------------------|-----------------------------|
| **Process Control**    | `CreateProcess()`              | `fork()`                    |
|                        | `ExitProcess()`                | `exit()`                    |
|                        | `WaitForSingleObject()`        | `wait()`                    |
| **File Management**    | `CreateFile()`                 | `open()`                    |
|                        | `ReadFile()`                   | `read()`                    |
|                        | `WriteFile()`                  | `write()`                   |
|                        | `CloseHandle()`                | `close()`                   |
|                        | `SetFileSecurity()`            | `chmod()`, `chown()`        |
|                        | `InitializeSecurityDescriptor()` | `umask()`, `setfacl()`   |
| **Device Management**  | `SetConsoleMode()`             | `ioctl()`                   |
|                        | `ReadConsole()`                | `read()`, `write()`         |
| **Information Management** | `GetCurrentProcessID()`    | `getpid()`                  |
|                        | `SetTimer()`                   | `alarm()`, `sleep()`        |
| **Communication**      | `CreatePipe()`                 | `pipe()`                    |
|                        | `CreateFileMapping()`          | `shmget()`, `mmap()`        |

