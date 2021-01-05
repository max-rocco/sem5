# Q. Explain segmentation & paging mechanism in 80386.

A. **Segmentation**

→ The memory management unit (MMU) consists of a segmentation unit and a paging unit. 
The segmentation unit allows the use of two address components, such as segment and offset for relocabilityand sharing of code and data. 
The segmentation unit allows segments of size 4Gbytes at maximum. 
  The segmentation unit provides a four level protection mechanism for protecting and isolating the system's code and data from those of the application program.

**Descriptors**

→ Every segment has a descriptor. When the programmer creates a logical segment, the system software
creates the corresponding descriptor with the help of compilers and loaders, linkers. It is the job of
operating system. Descriptors contain the information about segment. 
The 80386 descriptors have a 20- bit segment limit and 32-bit segment address. 
The descriptors of 80386 are 8-byte quantities containing access right or attribute bits along with the base and limit of the segments.

**Descriptor Tables**

→ In any system, there will be number of segments of various types created for various applications. 
Thus, there should be as many descriptors too. All these descriptors are stored in tables called descriptor tables. 
These tables are created by system software and stored in memory. 
The segmentation scheme provides a way of offering protection to different types of data and code.

**Descriptor Attribute Bits**

- The A (accessed) attribute bit indicates whether the segment has been accessed by the CPU or not.
- The TYPE field decides the descriptor type and hence the segment type.
- The S bit decides whether it is a system descriptor (S=0) or code/data segment descriptor (S=1).
- The DPL field specifies the descriptor privilege level.
- The D bit specifies code segment operation size. If D=l, the segment is a 32-bitoperand segment, else, it is a 16-bit \* operand segment.
- The P-bit (present) signifies whether the segment is present in the physical memory or not. If P=l, the segment is present in the physical memory.
- The G (granularity) bit indicates whether the segment is page addressable. The zero-bit must remain zero for compatibility with future processors.
- The AVL (available) field specifies whether the descriptor is available for user or for the operating system.

B. **Paging**

→ Paging is one of the memory management techniques used for virtual memory multitasking operating system.
* The segmentation scheme may divide the physical memory into a variable size segments but the paging divides the memory into a fixed size pages.
* The segments are supposed to be the logical segments of the program, but the pages do not have any logical relation with the program.
* The pages are just fixed size portions of the program module or data. 

→ The advantage of paging scheme is that the complete segment of a task need not be in the physical memory at any time. 
Only a few pages of the segments, which are required currently for the execution need to be available in the physical memory. 
Thus the memory requirement of the task is substantially reduced, relinquishing the available memory for other tasks.
Whenever the other pages of task are required for execution, they may be fetched from the secondary storage.
The previous page which are executed, need not be available in the memory, and hence the space occupied by them may be relinquished for other tasks.
Thus paging mechanism provides an effective technique to manage the physical memory for multitasking systems.

**Paging Unit** 
* The paging unit of 80386 uses a two level table mechanism to convert a linear address provided by segmentation unit into physical addresses.
* The paging unit converts the complete map of a task into pages, each of size 4K. The task is further handled in terms of its page, rather than segments.
* The paging unit handles every task in terms of three components namely page directory, page tables and page itself.

![](assets/80386-paging-1.png)

<hr />

Sources:

- http://teccmp.blogspot.com/2016/05/segmentation-of-80386-processor.html
- https://nptel.ac.in/content/storage2/courses/106108100/pdf/Teacher_Slides/mod8/M8L1.pdf
