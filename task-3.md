
## Base Integer ISA Encoding




![image](https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/b2fc7cc0-6b42-4cce-92b0-41a3d9ccf773)







• 32-bit fixed-width, naturally aligned instructions

• rd/rs1/rs2 in fixed location, no implicit registers

• Immediate field (instr[31]) always sign-extended

• Instruction Encoding Types

– R-type– Register

– I-type– Immediate

– S-type – Stores

– U-Type – Loads with immediate

• Reserved opcode space for custom instructions

– This opcode space will not be used by future
standard extensions

– instr[6:0] = 0b0001011 and 0b0101011




## Fence Instructions



<img width="238" alt="image" src="https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/1aa939d4-6779-4986-9792-3492347b0a20">





• Fences are used to enforce program order
on device I/O and memory accesses

• FENCE instruction format

– FENCE predecessor, successor

– Predecessor/successor can be

• R,W,I,O

– FENCE RWIO, RWIO – full barrier





## CSR and ECALL Instructions


• Control and Status Registers (CSRs) have their own dedicated
instructions :
– Read/Write
– Read and Set bit
– Read and Clear bit

• Environment Call instruction used to transfer control to the
execution environment and a higher privileged mode
– Triggers a synchronous Interrupt (discussed later)
– Example: User mode program can use an ECALL to transfer control to
a Machine mode OS kernel, aka System Call























<img width="352" alt="image" src="https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/ae5f4fca-8b24-4d03-b4c6-c5014f46e744">
