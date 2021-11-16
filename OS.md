1) OS is an interface between user and computer hardware.
2) System call is a request made by the user program to OS in order to get any kind of service.
3) OS is also called as resource allocator.
4) The primary goal of OS is convenience(easy to use) and secondary goal is efficiency(stability).
5) Batch OS: If the job is completed completely then only another job will be scheduled onto the CPU. Increased CPU idleness and decreased throughput of the system.
6) Number of jobs completed per unit time is called throughput of the system.
7) Multiprogramming OS: If the job is leaving CPU to perform I/O operation then another job which is ready for execution will be scheduled onto the CPU. Increased CPU utilisation and throughput of the system. Eg- Windows, UNIX.
8) Multitasking OS: Extension of Multiprogramming OS. Jobs will be executed in time sharing mode. Eg- Windows, UNIX.
9) Multiprocessor Systems: Fault tolerant Systems (if one CPU fails other works). Eg- UNIX
10) Real time Systems: The systems which are strict deadly time bound are called as real time systems. 
     i) Soft Real time Systems: Banking Sector (Minor delay accepted)
     ii) Hard Real time Systems: Satellite System, Missile Systems, etc.
11) Dual Mode operation: User Mode - Non - Privileged mode and Kernel mode - Privileged mode
12) Mode bit: Kernel mode - 0 and User mode - 1
13) Kernel mode - System mode / Supervisory mode / Monitor mode
14) The dual mode operation is used to provide protection and security to user programs and also to the OS from unauthorised users.
15) In the boot time system always starts in kernel mode.
16) The mode switching takes very less compared to process switching.
17) Privileged instructions: I/O operation, Context switching, Disabling the interrupts, setting time of clock, clearing and changing memory map
18) Non - Privileged instructions: reading the status of processor, reading time of clock, sending final print output to printer.
19) Layered approach of OS :
      i) layer1: process management 
      ii) layer2: memory management 
      iii) layer3: file management 
      iv) layer4: device management 
      v) layer5: protection and security
20) Advantage of layered approach: modularity, abstraction and debugging
21) Modularity means if any specific layer is getting updated, it will not have any impact on other layer.
22) if pid < 0 then child process creation failed else if pid == 0 then child process else parent process.
23) fork is a system call used to create child process.
24) fork return +ve value (process id of child process) to the parent process.
25) When the child process is created using fork() the new memory location will be allocated to child process.
26) the parent and child process will have same virtual address but different physical address.
27) n fork calls = 2^n - 1 child process
28) The program under execution is called process. It should reside in main memory.
29) process attributes:
      i) process id
      ii) process state
      iii) priority
      iv) program counter
      v) GPRs
      v) list of open files, devices
      vi) protection information
30) process id: unique identification number given by OS at the time of process creation
31) process state: contains current state info of process where it is residing.
32) program counter: contains address of the next instruction to be executed.
33) All attributes of process is called context of process. It is store in PCB.
34) Every process will have its own PCB.
35) PCB of processes will be stored in main memory and implemented using DLL.
36) Various states of process:
      i) New
      ii) Ready
      iii) Run
      iv) Wait or block
      v) termination or completion
      vi) suspend ready
      vii) suspend wait or suspend block
37) Various operations performed on process:
      i) creation
      ii) scheduling
      iii) dispatching
      iv) executing
      v) termination
      vi) suspending
      vii) resuming
38) process state diagram:
      i) Initially process will be in new state, it means process is under creation.
      ii) once process is created, it will be moved to ready state where there can be multiple processes.
      iii) one of the process from ready state is selected and dispatched to running state.
      iv) in running state, there can be only 1 process at a time.
      v) if a process needs I/O operation, it moves to wait/block state.
      vi) in wait state, there can be multiple processes.
39) when process is in ready, running or block state, it is residing in main memory.
40) if the resources are not sufficient to manage in ready state the some of the processes will be suspended and moved onto suspend ready state.
41) when process is in suspend ready state, then it is residing in backing store(secondary memory).
42) degree of multiprogramming: the number of processes present in main memory at any point of time is called as degree of multiprogramming.
43) CPU bound process: processes that require more amount of CPU time. they spend more time in running state.
44) I/O bound process: processes that require more amount of I/O time. they spend more time in wait/block state.
45) each and every time the process change its state, the context of the process will change as process state is a part of its attribute.
46) Context switching: saving the context of 1 process and loading the context of another process is called context switching.
47) If context of a process is more, the context switching time will also increase which is undesirable.
48) Context switching : burden for system
49) if there is only 1 process still it is called as context swtching. Round robin scheduling with 1 process.
50) OS schedulers:
       i) LTS or job scheduler: responsible for creating and bringing new process into the system.
       ii) STS or CPU scheduler: responsible for selecting one process from ready state to dispatch on running state.
       iii) MTS or medium term scheduler: responsible for suspending and resuming process. The job done by MTS is called swapping.
51) Dispatcher: responsible of loading the selected job onto the CPU. Also responsible for context switching.
52) LTS controls degree of multiprogramming.
53) Arrival time: the time when process arrives in ready state.
54) Turn Around time: CT - AT
55) Waiting time: TAT - BT
56) Response time: time difference between first response and arrival time
57) Goal of cpu scheduling: to maximise cpu utilisation, throughput of system and to minimise avg WT, TAT, RT.
58) Convoy effect: In FCFS, if 1st process is CPU bound (large BT) followed by many I/O bound processes (small BT), then it will have major effect on avg WT of process because small process will have to wait for larger duration.
59) In RR, if time quantum is less then no of context switches will increase and response time will be less.
60) In RR, if time quantum is more then no of context switches will decrease and response time will be more.
61) In RR, if time quantum is more than all BT, it behaves like FCFS.
62) 
