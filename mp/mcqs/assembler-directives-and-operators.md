## Microprocessors Questions and Answers – Assembler Directives and Operators

1. The assembler directives which are the hints using some predefined alphabetical strings are given to

* [ ] processor
* [ ] memory
* [x] assembler
* [ ] processor & assembler

Explanation: 
These directives help the assembler to correctly understand the assembly language programs 
to prepare the codes.

<hr />

2. The directive used to inform the assembler, the names of the logical segments to be assumed 
for different segments used in the program is

* [x] ASSUME
* [ ] SEGMENT
* [ ] SHORT
* [ ] DB

Explanation: In ALP, each segment is given a name by using the directive ASSUME.

```
Syntax
ASSUME segment:segment_name

Example
ASSUME CS:Code
```

<hr />

3. Match the following

```
a) DB     1) used to direct the assembler to reserve only 10-bytes
b) DT     2) used to direct the assembler to reserve only 4 words
c) DW     3) used to direct the assembler to reserve byte or bytes
d) DQ     4) used to direct the assembler to reserve words

```

* [ ] a-3, b-2, c-4, d-1
* [ ] a-2, b-3, c-1, d-4
* [ ] a-3, b-1, c-2, d-4
* [x] a-3, b-1, c-4, d-2

Explanation: These directives are used for allocating memory locations in the available memory.
