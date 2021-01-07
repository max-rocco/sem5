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

<hr />

4. The directive that marks the end of an assembly language program is

* [ ] ENDS
* [x] END
* [ ] ENDS & END
* [ ] None of the mentioned

Explanation: The directive END is used to denote the completion of the program.

<hr />

5. The directive that marks the end of a logical segment is

* [x] ENDS
* [ ] END
* [ ] ENDS & END
* [ ] None of the mentioned

Explanation: The directive ENDS is used to end a segment where as the directive END is used to end the program.

<hr />

6. The directive that updates the location counter to the next even address while executing a series of instructions is

* [ ] EVN
* [x] EVEN
* [ ] EVNE
* [ ] EQU

Explanation: The directive updates location counter to next even address if the current location counter contents are not even.

<hr />

7. The directive that directs the assembler to start the memory allotment for a particular segment/block/code from the declared address is

* [ ] OFFSET
* [ ] LABEL
* [x] ORG
* [ ] GROUP

Explanation: If an ORG is written then the assembler initiates the location counter to keep the track of allotted address for the module as mentioned in the directive.
If the directive is not present, then the location counter is initialized to 0000H.

<hr />

8. The directive that marks the starting of the logical segment is

* [ ] SEG
* [x] SEGMENT
* [ ] SEG & SEGMENT
* [ ] PROC

Explanation: The directive SEGMENT indicates the beginning of the segment.

<hr />

9. The recurrence of the numerical values or constants in a program code is reduced by

* [ ] ASSUME
* [ ] LOCAL
* [ ] LABEL
* [x] EQU

Explanation: In this, the recurring/repeating value is assigned with a label. The label is placed instead of the numerical value in the entire program code.

<hr />

10. The labels or constants that can be used by any module in the program is possible when they are declared as

* [ ] PUBLIC
* [ ] LOCAL
* [x] GLOBAL
* [ ] Either PUBLIC or GLOBAL

Explanation: The labels, constants, variables, procedures declared as GLOBAL can be used by any module in the program.

<hr />

Sources

* https://www.sanfoundry.com/microprocessors-mcqs-assembler-directives-operators/
