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
62) Highest Response Ratio Next(HRRN) : Non preemptive.  Response ratio = (w + s) / s where w = waiting time and s = burst time.
63) HRRN favours shorter jobs and limits the waiting time of longer jobs.
64) Multilevel queue scheduling: high priority process placed in top level ready queue and low priority process in bottom level ready queue.
65) Only after completion of all process in top level ready queue further level ready queue processes will be scheduled.
66) If this is the strategy, then processes in bottom level ready queue suffer from starvation.
67) Starvation: Indefinite waiting of a process.
68) To avoid the problem of starvation, the concept of ageing is used.
69) Ageing: If the waiting time of a process increases, then priority of that process will be increased.
70) Multilevel feedback queue scheduling: every process will definitely get a chance to execute but still there is a possibility of starvation.
71) No starvation in : FCFS, LRTF, RR, HRRN
72) The execution of one process affects or affected by other processes then those processes are said to be co-operative processes otherwise they are said to be independent processes.
73) If the processes are not properly synchronised then problems can be : inconsistency, loss of data, deadlock.
74) Critical section: The portion of program text where shared resources/variables will be placed.
75) Non CS: independent code of the process will be placed.
76) Race condition: the final value of any variable depends on the execution sequence of the processes. To avoid race condition, only 1 process is allowed to enter in CS.
77) the conditions to be followed to achieve synchronisation:
       i) ME: Only 1 process in CS at any time
       ii) progress: No process running outside the CS should block the other interested process from entering in CS when CS is free.
       iii) bounded waiting: No process should have to wait forever to enter in CS. If bounded waiting is not satisfied, then it is possible for starvation.
       iv) no assumptions related to hardware and processor speed.
78) step no.3 solutions:
       i) s/w type: lock variables, strict alteration or deckers algo, petersons algo
       ii) h/w type: TSL instruction set
       iii) OS type: counting and binary semaphore
       iv) programming language compiler support type: monitors
79) Lock varibales: ME and bounded waiting is not satisfied
80) Strict Alteration(process takes turn to enter in CS): progress is not satisfied.
81) If any solution is having deadlock, progress is not satisfied.
82) petersons algo(2 process solution): All 3 satisifed. correct solution
83) TSL instruction set: copies the current value of flag in register and stores the value of "1" into flag in a single atomic cycle without any preemption.
84) TSL: ME and progress satisfied but bounded waiting not
85) even in RR bounded waiting is not satisfied.
86) if some process is in CS the other process outside CS which are trying to enter in CS will be busy in waiting checking all 3 conditions this is called busy waiting also called as spin lock.
87) to avoid busy waiting the concept of semaphore is used.
88) semaphore is an integer variable which is used by various processes in a mutual exclusive manner to achieve synchronisation.
89) down() or wait() or p() and up() or signal() or v() or release()
90) after performing down operation if process is getting suspended, then it is called unsuccessful down operation otherwise successful down operation.
91) suspended process PCB placed in suspended list.
92) up operation is always successful.
93) Every semaphore variable will have its own suspended list.
94) If two or more processes are in suspended list and there is no other process to wake up them then those processes are said to be in deadlock.
95) Dining philospher: take left fork and then right fork but if all philospher are hungry at same time then they will be in deadlock.
96) monitor is collection of variables, condition variables and procedures combined together in a special kind of module or package.
97) The process running outside the monitor can't access the internal varables of the monitor but they can call the procedures of montor.
98) Only one process can be active inside monitor at any time.
99) Concurrent programming: possible only on multiprocessor systems.
100) Concurrent has 3 different meanings: they can execute concurrently or parallely, they do not have any dependency, anyone can start first.
101) 2 or more processes waiting for some event to happen and that never happens then they are said to be in deadlock.
102) Resource Allocation Graph : Resource request and resource allocation will be presented using RAG.
103) Deadlock characteristics: Mutual Exclusion, Hold and wait, No preemption, Circular Wait.
104) Mutual Exclusion : The resource has to be allocated to only 1 process or it should be freely available.
105) No preemption: The resource has to be voluntarily released by the process after completion of execution. Not allowed tro forcefully preempt the resource
106) If all 4 cnditions are there then it is deadlock.
107) Deadlock prevention: 
      i) Eliminate Mutual exclusion : It is not always possible to dissatisfy the mutual exclusion because some resources, such as the tape drive and printer, are non-                                             shareable.
      ii) Eliminate Hold and wait : Allocate all required resources to the process before the start of its execution, this way hold and wait condition is eliminated but it                                       will lead to low device utilization. 
                                    The process will make a new request for resources after releasing the current set of resources. This solution may lead to starvation.
      iii) Eliminate no preemption : Preempt resources from the process when resources required by other high priority processes. 
      iv) Eliminate circular wait : Resources will be assigned with unique numbers. The process can request for resources only in increasing or decreasing order of numbering.
108) Deadlock avoidance : Banker's Algorithm 
109) If the system is in unsafe state, then it is possible for deadlock.
110) The order in which we satisfy the remaining needs of processes is called safe sequence.
111) Deadlock avoidance is less restrictive than deadlock prevention. As in Deadlock prevention, request for a resource may not be granted even if the resulting state is safe but in deadlock avoidance, request for a resource is granted if the resulting state is safe.
112) Deadlock detection: If all resources are of single instance type then cycle in RAG is sufficient and necessary condition for deadlock.
113) If all resources are NOT of single instance type then cycle in RAG is necessary condition for deadlock NOT SUFFICIENT.
114) Deadlock recovery:
        I) kill process
            i) kill all processes involved in deadlock.
            ii) kill one after other
                a) kill low priority first
                b) kill on basis of percentage completion
                c) based on resources holding and requesting by processes
        II) Resource preemption:
              Resoucre preempted from process which are involved in deadlock and given to other processes so that there is a chance of recovery. But it can lead to starvation
        III) Ostrich Algo : Ignore deadlock
115) Thread is light weight process (no. of instruction will be less and context will be less)
116) Advantages : 
        i) Responsiveness : process divided into threads then if one thread completes the excecution, then output will be responded immediately. Response faster than process.
        ii) Faster context switches : due to less context.
        iii) Effective utilisation of multiprocessor systems: Threads running on different processor so that process execution will be faster.
        iv) Resource sharing: Resources except stacks and registers are shared. Resources like code, data, files, global variables,heap and memory will be shared. Every                                     thread will have its own stacks and registers.
        v) Enhanced throughput of system: As process divided into multiple threads and each thread is a job.
        vi) Economical
117) User level and kernel level threads: 
        i) User level threads are implemented by user but kernel level threads are implemented by OS
        ii) Os can't recognise user level threads as for OS user level threads are just process but kernel level threads are recognised by OS.
        iii) If one user level thread is performing blocking system call then entire process will go into block state but this is not the case with kernel level threads.
        iv) User level threads are dependent but kernel level threads are not.
        v) Implementation of user level threads is easy but complicated for kernel level threads.
        vi) User level threads have less context while kernel level threads have more.
        vii) No H/W level support is required for user level threads.
118) "GANG" scheduling is used in threads.
119) Synchronous I/O : The process performing I/O operation will be placed in block state till I/O operation is completed. Once I/O operation is completed, ISR (INTERRUPT SERVICE ROUTINE) will initiate and brings process from block to ready state.
120) Asynchronous I/O: While initiating I/O request, the handler function will be registered. The process is not placed in block state and it continues to execute the reamining code after initiating I/O request. Once I/O operation is completed, the signal mechanism is used to notify the process that data is available and registered handler function will be asynchronously invoked.
121) OS allocates and deallocates memory to the process. Main goal is to efficiently utilise memory by minimising internal and external fragmentation.
122) Capacity of memory = no. of words in memory * word size
123) Loading : Bringing process from secondary memory to main memory is called as loading.
124) Linking : Establishing the linking between all modules or all the functions of program in order to continue program execution.
125) Static loading : Loading entire program in memory before start of program execution is called as static loading.
126) Static loading : inefficient use of memory, program execution will be faster, if static loading then always static linking.
127) Dynamic loading: loading the program into memory on demand is called dynamic loading.
128) Dynamic loading : efficient use of memory, program execution will be slower, if dynamic loading then always dynamic linking.
129) Addess binding: Association of program instructions and data to the actual physical memory loactions is called as address binding.
130) Compiler time Address Binding : compiler is responsible for compile time AB. This type of AB will be done before loading the program in memory. The compiler needs to interact with OS memory manager to perform compile time AB.
131) Load time AB : This type of AB will be done after loading the program in memory. The load time address binding will be done by OS memory mananger(loader)
132) Execution time or Dynamic AB: The AB will be postponed even after loading the program in memory. The program will keep on changing loactions in memory till time of program execution. This type of address binding will be done by processor at the time of program execution.
133) Majority of OS perform dynamic loading, linking, address binding.
134) Fixed partition scheme : memory will be divided into fixed partitions, in every partition, only 1 process will be allocated. Degree of multiprogramming is restricted by no. of partitions in memory. Maximum size of process is restricted by max size of partition. Every partition is associated with limit registers (lower limit (starting address of partition), upper limit (ending address of partition))
135) Variable partition scheme : initially, memory will be single continous free block. whenever process comes, partition will be made in memory.
136) External fragmentation happens when there’s a sufficient quantity of area within the memory to satisfy the memory request of a method. however the process’s memory request cannot be fulfilled because the memory offered is during a non-contiguous manner.
137) Techniques used to avoid external fragmentation: 
       i) compaction : moving all processes to top or bottom  to make free available memory in single continuous place. undesirable to implement because it affects all                              running process in memory.
       ii) implementing non contiguous memory management techniques : best fit, first fit, next fit, worst fit
           a) best fit - smallest sufficient
           b) worst fit - largest sufficient
           c) first fit - first sufficient
           d) next fit - first sufficient from last allocation point
138) Paging: The technique of mapping CPU generated logical address to physical address is called as paging.
139) Logical Address space is divided into equal size pages.
140) Physical address space is divided into equal size frames.
141) Page size = frame size
142) Whenever paging is applied page table has to be maintained.
143) No. of entries in page table is same as no. of pages in LAS.
144) Page table entry (PTE) contains frame number.
145) Page tavle is also called as address transalation table.
146) Frame number is also called as translation bits.
147) LA is divided into 2 parts p and d where p = no. of bits required to represent pages of LAS or page number and d = no. of bits required to represent page size.
148) PA is divided into 2 parts f and d where f = no. of bits required to represent frames of PAS or frame number and d = no. of bits required to represent frame size.
149) Paging is wrt every process and every process will have it's own page table and the base address of page table is stored in PCB.
150) Page tables of processes will be store in main memory.
151) NO external fragmentation in paging.
152) Internal fragmentation in last page i.e equal to p/2 where p = page size
153) Maintaining page table is overhead for system.
154) PTE contains frame number (transalation bits) but along with it sometimes it may contain additional bits like 
        i) valid/invalid bit or present bit (page available in main memory or not)
        ii) dity or modified bit   (page modified by processor or not)
        iii) reference bit  (how many times page is referred by processor)
        iv) page protection or permission bits  (used for protection and security from unauthorised access)
155) Page table size = no. of entries in page table * PTE size
156) Performance of paging: Main memory access time = 'm'. page tables stored in main memory. EMAT = 2m
157) TLB (Translation look aside buffer is added to improve the performance of paging. TLB is H/W device implemented using associative registers. It contains frequently referred page numbers and corresponding frame numbers. TLB access time is very less.
158) EMAT = x(c + m) + (1 - x)(c + 2m)  where x = TLB hit ratio and c = TLB access time.
159) To avoid the overhead of maintaining large size page table in main memory, MULTILEVEL PAGING is implemented.
160) In MULTILEVEL PAGING, paging will be applied on page table and instead of bringing entire Page table into memory, the pages of page table will be brought in memory.
161) EMAT for n-level paging : x(c + m) + (1 - x)(c + (n + 1) * m)
162) In multilevel paging when paging is applied on page tables the last page table which we get is called as 1st level page table.
163) In multilevel paging when paging is applied on page tables then 1st level page table entry contains base address of second level page table, the 2nd level PTE contains base address of 3rd level page table and so on. The final PTE contains frame number of actual page.
164) In multilevel paging, all page tables are stored in main memory.
165) To avoid overhead of maintaining page table for every process inverted paging will be implemented.
166) In inverted paging, only 1 page table will be maintained for all processes.
167) No. of entries in page table = No. of frames in PAS.
168) Paging does not follow user's view of memory allocation.
169) To achieve user's view of memory allocation, segmentation will be implemented.
170) In segmentation, LAS will be divided into segments.
171) Segments of LAS will vary in size and brought into PAS.
172) No. of entries in segment table is same as no. of segments in LAS.
173) Segmentation suffers from external fragmentation.
174) To avoid the overhead of bringing large size segment into memory, segmented paging will be implemented.
175) In segmented paging, paging will be applied on segment and instead of bringing entire segment in memory the pages of segment will be brought in memory.
176) No. of entries in page table of segment is same as no. of pages on segment.
177) Page size of segment is same as frame size of PAS.
178) Buddy system: Initially memory is single continuous free block.
179) Whenever request by process arrives memory will be divided into 2 half blocks.
180) If request by process is too small then the lower block of memory is further divided into 2 half blocks again.
181) In buddy system, memory will be allocated from lower to higher blocks.
182) Virtual memory gives an illusion to the programmer, that the programs of larger size than actual physical memory can be executed.
183) Virtual memory is implemented using demand paging and demand segmentation.
184) Demand paging: Loading the page into memory on demand (whenever page fault occurs)
185) Page fault: The CPU is trying to refer the page in main memory but the page is currently not available in the PAS.
186) The program execution will stop and signal will be sent to OS regarding page fault.
187) OS will search for required page in LAS.
188) The required page will be brought from LAS to PAS through page replacement algo.
189) The respective page table entry will be updated accordingly.
190) Signal will be sent to CPU to continue program execution and CPU will access the required page in main memory and continue program execution.
191) EMAT : p * s + (1 - p) * m  (p = page fault rate, s = PFST, m = MMAT)
192) No. of frames allocated to the process is decided by ISA (Instruction Set Architecture)
193) Belady's anomaly: In FIFO page replacement algo, by increasing no. of frames to the process the no. of page faults should decrease but they are increasing.
194) Optimal page replacement : which is not used for longest duration of time in future.
195) Thrashing : Thrashing is when the page fault and swapping happens very frequently at a higher rate, and then the operating system has to spend more time swapping these pages. This state in the operating system is known as thrashing. Because of thrashing, the CPU utilization is going to be reduced or negligible.
196) Causes of thrashing: 
        i) High degree of multiprogramming
        ii) Lack of frames (Main memory)
197) Recovery of thrashing:
        i) Don't allow the system to go into thrashing and instruct the LTS not to bring the processes into memory after point of lambda.
        ii) If the system is already in thrashing then instruct the MTS to suspend some of the processes so that we can recover the system from thrashing.
198) The main purpose of virtual memory is to increase degree of multiprogramming.
199) If we remove virtual memory then efficient implementation of multiprogramming and multiuser is not possible.
200) All attributes of file is called file context and they are stored in FCB.
201) Access methods of file : Sequential and random access
202) Disk space allocation methods: 
       i) Contiguous allocation : Disk block allocated in continuous manner, every file is associated with 2 parameters a)starting disk block address b)size
                                  Increasing file size may not be possible always, suffering from external fragmentation, internal fragmentation exists in last disk block of                                   file. Supports both sequential and random access.
       ii) Linked/Non contiguous allocation: increasing file size always possible if disk block is available, NO external fragmentation, internal fragmentation in last disk                                                block of file, overhead of maintaining pointer in every disk block, if pointer lost then file will be truncated, supports only 
                                             sequential access.
       iii) Indexed Allocation: every file is associated with its own indexed node, indexed nodes contains all disk block addresses of file, disk blocks are allocated in non                                 contiguous manner, NO external fragmemtation, internal fragmentation in last disk block. if file size large then 1 disk block will not be 
                                sufficient to contain all DBAs but file size small then its a wastage.
       iv) UNIX I-Node implementation  -----> an extension of INode implementation. every file is associated with its own I-Node. Whenever the file is created depending on                                                 size of file, file will be stored in direct DBA, or maybe in single indirect DBA, or maybe in double indirect DBA.
203) No. of DBA's one DB can contain = DB size / DBA
204) If context switching is diabled then process is not allowed for preemption.
205) In free list approach: some disk block are used just to store the free disk block addresses.
206) In bit map approach every disk block will be mapped with 1 binary bit.
207) Disk scheduling: To minimise average seek time of disk.
