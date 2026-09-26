# risc-v-
This repository contains my understanding about RISC V and CPU working
# Working of CPU
## CPU
1. ALU  
2. CU
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



