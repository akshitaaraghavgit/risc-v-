# risc-v-
This repository contains my understanding about RISC V and CPU working
# Working of CPU
## CPU
1. ALU ( Arithmatic logic unit ) 
2. CU ( control unit )
3. Registers
  -RAM
## Pipelining Process
1. ### Fetch
    - Get instruction from memory (RAM)
    - Store in Instruction Register(IR)          
2. Decode
   - Decoding is done by CU
3. Execute
   - Alu does execution
4. Write back
   -Done by CU
## Registers
-They are tiny storage locations inside CPU
- Fetching data from register is 100x faster than fetching data from RAM
- While RAM contains both instructions and data, registers store data only
# RISCV
 It defines how to write instructions for CPU
 It consists a total of 150 instructions, so it doesn't complicate the CPU.
 It makes instructions independant.
- It has a total of 32 registers(0x - 31x)

## Project 1: Sum from 1 to 5 in RISCV
<img width="1878" height="795" alt="Screenshot 2026-09-26 165230" src="https://github.com/user-attachments/assets/4886cc03-670d-494c-9abd-1b2c5808ec27" />


<img width="1886" height="827" alt="Screenshot 2026-09-26 163621" src="https://github.com/user-attachments/assets/b189a0f0-e659-4cac-8fdf-5b3d10ea793f" />

## Explaination
Here I have used 3 registers
x5,x6,x7 where x6 is the counter
### Use of loop
bne(branch if not equal)- this instruction is used for loop, it will continue iterating until x6==x7
value of counter x6 keeps incrementing by 1 in each successive iteration.
When the value of x6==x7 the loop stops

### Labels
main,loop, end are the labels

### ecall instruction
Terminates the program

### Connection of this project to CPU Architecture
1. Control Unit decodes each instruction
2. ALU performs the addition ( adder )
3. Use of registers
# Memory Hierarchy
- A computer has several kinds of memory stacked in layers.
- Can be understood by thinking of a pyramid-the smallest, fastest memory sits at the top, closest to the CPU; the biggest, slowest memory sits at the bottom, furthest away.
## Why This Hierarchy Exists?
- Fast memory is expensive and takes chip area
- Cheap memory is slow
-  Programs need lots of data but only use small portions actively
## Solution: 
- Use small amounts of fast memory for active data, larger amounts of slower
memory for less active data.
- CPU Registers-Currently active data
- L1 Cache-Recently used instructions/-
data
- L2 Cache-Less recently used data
- L3 Cache-Shared cache between cores
- Main memory-Program storage
- ssd-Long-term file storage
- hard drive-bulk storage
# Virtual Memory
- Virtual address-the fake address every individual uses
- Physical address-where the data actually gets stored inside RAM
## Address Translation-
- MMU (Memory Management Unit)-it takes the virtual address the program used and produces the real physical address that actually gets sent to RAM
# RISC-V Register Set
- RISC-V has 32 general-purpose registers (x0-x31) plus special registers
## The Special x0 Register
- Register x0 is hardwired to always contain zero
### Uses of x0
<img width="770" height="457" alt="Screenshot 2026-09-30 233019" src="https://github.com/user-attachments/assets/a221b9f9-d856-4fda-885a-dde0a4fea3e7" />

  
  
 



