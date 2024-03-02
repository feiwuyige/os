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