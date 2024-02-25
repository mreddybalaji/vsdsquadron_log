# vsdsquadron_log
This repository contains all the resources for the VSDSquadron Research Internship 



# RISC-V

A high-quality, license-free, royalty-free RISC ISA

• Standard maintained by the non-profit RISC-V Foundation

• Suitable for all types of computing systems
from Microcontrollers to Supercomputers

•RISC-V is available freely under a permissive license

• RISC-V is not…
– A Company
– A CPU implementation


## Specificitations

• User Mode (Unprivileged ISA)

• Privilege Mode




## Instruction Set 



![image](https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/bd619147-e1b0-4dbb-80ff-3acbbd883314)


• ISA Name format: RV[###][abc…..xyz]


– RV – Indicates a RISC-V architecture


– [###] - {32, 64, 128} indicate the width of the
integer register file and the size of the user
address space


– [abc…xyz] – Used to indicate the set of
extensions supported by an implementation.




## Extensions:


<img width="218" alt="image" src="https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/029d6230-7715-40a6-91c7-ca4a033d8bd6">




• Extensions define instructions
– “I” for Integer is the only required extension in a RISC-V
implementation and defines 40 instructions

• The RISC-V Specification defines a number of “Standard
Extensions”
– Standard Extensions are defined by the RISC-V Foundation
and are optional

• RISC-V allows for custom, “Non-Standard”, extensions in
an implementation

• Putting it all together (examples)
– RV32I – The most basic RISC-V implementation
– RV32IMAC – Integer + Multiply + Atomic + Compressed
– RV64GC – 64bit IMAFDC
– RV64GCXext – IMAFDC + a non-standard extension





## Registers:


<img width="302" alt="image" src="https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/e93a1592-95f8-4977-a583-b95c1f7171ed">




• RV32I/64I have 32 Integer Registers
– Optional 32 FP registers with the F
and D extensions
– RV32E reduces the register file to 16
integer registers for area constrained
embedded devices

• Width of Registers is determined by ISA

• RISC-V Application Binary Interface (ABI)
defines standard functions for registers
– Allows for software interoperability
• Development tools usually use ABI names
for simplicity








