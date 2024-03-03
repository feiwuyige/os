# OSTEP

## The Abstraction:The Process

1. Process:it is a running program,the abstraction provided by the OS of a running program.
2. Process's machine state:
   * **address space** : the memory that the program can address.
   * **registers** : many instructions explicitly read or update registers,so it is important to the execution of the process.
   * ....
3. Process API : some idea of what must be included in any interface of an operating system.
   * **Create :** create new process.
   * **Destroy :** kill the process.
   * **Wait :** wait for a process to stop running.
   * **Miscellaneous Control : ** for example, provide some kind of method to suspend a process and then resume it (continue it  running).
   * **Status : **get the status information of the process, such as how long it has run for.
4. Process creation:
   * Load the program's code and any static data into memory, into the address space of the process.
   * Some memory must be allocated for the program's **run-time** stack.
   * Os may allocate some memory for the program's **heap**.
   * Do some other initialization tasks, particularly as related to input/output.
5. Process States:
   * **running**: a process is running on a processor. It is executing instructions.
   * **ready**: a process is ready to run but for some reasons the OS has chosen not run it at this given time.
   * **block**: a process has performed some kind of operation that make it not ready to run until some other event take place.
6. **PCB(process control block)**: the structure that stores information about a process. 
7. You can think of the mechanism as providing the answer to a how question about a system; for example, how does an operating system perform a context switch? The policy provides the answer to a which question; for example,which process should the operating system run right now?

## Interlude: Process API

1. **fork()**: the process that is created is an (almost) *exact copy of the calling process*. The newly-created process comes into life as if it had called `fork()` itself.Notice that the value parents and child returns to the caller of `fork()` is different.Specifically, while the parent receives the PID of the newly-created child, the child receives a return code of zero.