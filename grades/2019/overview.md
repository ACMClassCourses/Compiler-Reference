# Compiler for Grade 2019

## Introduction
**Compiler 2021**

TAs: @peterzheng98, @ZYHowell, @fstqwq, @jinhongyii

## Course Grading
- Semantic Correctness: 60%
- Codegen Correctness: 15%
- Optimize: 19%
- Bonus: 6%

**No late submissions will be accepted.**

## Projects
Compiler: From Mx to RISC-V

Project homepage: https://github.com/ACMClassCourses/Compiler-Design-Implementation

S1: Semester 1 / WV: Winter Vacation / S2: Semester 2

Frontend: S1W18(Suggested)

Codegen: S2W5, IR for S2W3

Optimize: S2W9

Bonus: S2W16


## Policy
**Bonus:** You can only select one of the given topics.

**Checkpoints:** We will check the progress every three weeks, and some of them will be graded.

About groups: We will make several groups. Different groups will have different requirements and deadlines.
## Calendar
### Tutorials

| Time | Topic | Place | 
|-------|--------------------|---|
| 2020.11.26 10:00 | Parser and Lexer | East Upper Hall 107 |
| TBA | TBA | TBA |


### Checkpoints

**Check:** 1.2, 1.6, 2.1, 2.4, 2.7, 3.0, 3.3
1. Semantic:
    - 1.0 Yx Language: g4 files, AST Nodes
    - 1.1 Mx Language: g4 Files or lexer
    - 1.2 Mx Language: AST Nodes
    - 1.2b AST Printer(Optional)
    - 1.3 Scope and Class
    - 1.4 Type Check
    - 1.5a Statement Check
    - 1.5b Pass 50% Semantic Check
    - 1.5c Pass Semantic Check
    - 1.6 AST Optimizer(Optional)
2. Codegen:

| Stage | LLVM | User Design |
|-------|------|-------------|
|2.0a| IR Nodes Design | IR Nodes Design |
|2.0b| IR Nodes Impl | IR Nodes Impl |
|2.1| IR Builder | IR Builder |
|2.2| SSA | SSA(Optional) |
|2.3 (optional)| *N/A* | IR Intepreter |
|2.4| Check IR | Check IR |
|2.5a (optional)| Three-address Code | Three-address Code|
|2.5b| Instruction Selection | Instruction Selection | 
|2.6| Register Allocation | Register Allocation |
|2.7| Pass Codegen Test | Pass Codegen Test |

3. Optimize:
    - 3.0 Register Allocation
    - 3.1 DCE
    - 3.2 Inline
    - 3.3 CSE
    - 3.4 Pass Optimize Test
4. Bonus(TBA):
    - 4.1 JIT
    - 4.2 Debug information
    - 4.3 Class
