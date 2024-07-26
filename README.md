# Small-Process-Management-System-Priority-NPP-Dual-Core
A Python simulation of a small process management system with a priority non-preemptive scheduling system on Dual Core (2 Cores).
(has some issues; any version of this that is copied and used MUST be changed and shared on github to allow for growth, learning and improvement.)

The Project 
Your group has been asked to simulate a small process management system which will use a priority non-preemptive scheduling scheme when executing processes on a dual-core (2 CPU’s) processor system. The system manages twenty (20) processes and maintains a shared reusable resource that all processes will interact with; all processes perform some task on the shared resource (list of integer pairs). The system is capable of running up to two (2) processes concurrently. This prototype is aimed at demonstrating the concept of process synchronization by restricting access to the shared resource based on when processes are executing in its critical section.
At the beginning of the program the shared resource list should initialize all data values to 0. Given that multiple processes can generate the same task, and some tasks are updating the shared resource, there is a need to synchronize the execution. Adding and Removing tasks modify the shared list, while retrieve and calculate tasks simply read the shared data. Any task that modifies the shared list must have mutual exclusion on the shared resource while multiple processes executing retrieve and/or calculate tasks are able to do so concurrently. Adding and removing records has priority over record retrieval and tallying. When a process that is modifying the resource list gets selected from the ready queue and is added to a CPU, it must ensure that the process on the other CPU is completed before it locks and updates the resource list based on its task – during this time that process will be blocked. The program should end when all the processes have completed. 

Your team is allowed to implement the system in any of the following programming languages: Python, C, C++, C# or Java. 

The shared resource list (list of integer pairs) can hold up to twenty (20) records which contains: 
i.	Id (sequential list between 1 and 20)
ii.	Data value (integer )

A process can be executing any of the following tasks on the shared resource integer list: 
i.	Add Record: randomly generates a resource record and updates that record -  id (1-20) and data value (1-100)
ii.	Remove Record: randomly generates a record id (1-20) and sets that records data value to 0
iii.	Retrieve a Record: randomly generates a record id then reads and outputs the data value for that id.
iv.	Calculate Record Data Total: Sum and display all the data values in the resource list.

A process should contain: 
i.	PID (uniquely assigned between 1 and 20) 
ii.	Task (a randomly select option of the four above) 
iii.	Priority (integer value 1 – 5 with 1 being the highest) 
iv.	Arrival time (randomized number between 0 and 29) 
v.	Start time (system time) 
vi.	End time (system time) 
vii.	Blocked time (numeric value) 
viii.	Burst time (randomized number between 1 to 5 seconds) 

Expectation(s): 
1.	Process data structure must be implemented independent of the Shared Resource List data structure 
2.	Multiple processes can be generated with the same task 
3.	Implement the scheduling algorithm 
4.	Appropriate locking mechanism is used
5.	Regular details of all the processes as well as the state of the shared resource list at key intervals should be displayed during program execution so verification can be done
