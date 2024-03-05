
# VSDSQUADRON:

This repository contains all the resources and tasks for the VSDSquadron Research Internship.




## Task - 1: Tools Installation

## Yosys Installation:

```bash
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make
sudo apt-get install build-essential clang bison flex libreadline-dev gawk tcl-dev libffi-dev git graphviz xdot pkg-config python3 libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make install

```


![Screenshot from 2024-03-05 15-28-44](https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/6df8e52e-39df-4bb9-8f07-7cd01b454a1a)





## Iverilog Installation:
```bash
sudo apt-get install iverilog

```
## GTKWave Installation:
```bash
sudo apt update
sudo apt install gtkwave

```

![image](https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/af9ae1d4-9fa1-4b84-aae6-e26560c5fd0b)




## OpenSTA Installation:

```bash
git clone https://github.com/The-OpenROAD-Project/OpenSTA.git
cd OpenSTA
mkdir build
cd build
cmake ..
make
```


![image](https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/892ae43e-9dae-4f22-ba72-6dd7950d6d96)




## ngspice Installation:

```bash
tar -zxvf ngspice-37.tar.gz
cd ngspice-37
mkdir release
cd release
../configure  --with-x --with-readline=yes --disable-debug
make
sudo make install

```


![image](https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/f0834d2f-fff4-43d7-8f8f-77671f1c7eec)





## OpenLANE Installation:

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv python3-pip make git
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world
sudo groupadd docker
sudo usermod -aG docker $USER
sudo reboot
docker run hello-world

```


![image](https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/1ed49529-54dd-4538-88bb-f96a3c86fc8e)




## Magic Installation:

```bash
sudo apt-get install m4 tcsh csh libx11-dev tcl-dev tk-dev libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
make install
```






## Task - 2: RISC V Instruction Set:


## RISC-V Assembly Instructions Overview



### Instruction 1: Add
- **Type**: R-TYPE ARITHMETIC
- **Specification**: Performs addition on `r4` and `r3`, result in `r2`.
- **Encoding**: `0000000|r3|r4|000|r2|0110011`

### Instruction 2: Sub
- **Type**: R-TYPE ARITHMETIC
- **Specification**: Subtracts `r3` from `r4`, result in `r5`.
- **Encoding**: `0100000|r4|r3|000|r5|0110011`

### Instruction 3: And
- **Type**: R-TYPE LOGICAL
- **Specification**: Bitwise AND `r2` and `r4`, result in `r6`.
- **Encoding**: `0000000|r4|r2|111|r6|0110011`

### Instruction 4: Or
- **Type**: R-TYPE LOGICAL
- **Specification**: Bitwise OR `r3` and `r6`, result in `r1`.
- **Encoding**: `0000000|r6|r3|110|r1|0110011`

### Instruction 5: Xor
- **Type**: R-TYPE LOGICAL
- **Specification**: Bitwise XOR `r2` and `r5`, result in `r7`.
- **Encoding**: `0000000|r5|r2|100|r7|0110011`

### Instruction 6: Slt
- **Type**: R-TYPE LOGICAL
- **Specification**: Set `r8` to 1 if `r3` < `r5`, else 0.
- **Encoding**: `0000000|r5|r3|111|r8|0110011`

### Instruction 7: Addi
- **Type**: I-Type
- **Specification**: Adds immediate 10 to `r5`, result in `r9`.
- **Encoding**: `00000001010|r5|000|r9|0010011`

### Instruction 8: Sw
- **Type**: S-TYPE
- **Specification**: Store `r4` into memory at `r2` + offset 4.
- **Encoding**: `0000000|r4|r2|010|00100|0100011`

### Instruction 9: Lw
- **Type**: I-Type
- **Specification**: Load 32-bit value into `r10` from memory at `r2` + offset 4.
- **Encoding**: `000000000100|r2|010|r10|0000011`

### Instruction 10: Beq
- **Type**: B-TYPE
- **Specification**: Branch if `r1` equals `r1`.
- **Encoding**: `imm[12|10:5]|r1|r1|000|imm[4:1|11]|1100011`

### Instruction 11: Bne
- **Type**: B-TYPE
- **Specification**: Branch if `r1` not equals `r2`.
- **Encoding**: `imm[12|10:5]|r1|r2|001|imm[4:1|11]|1100011`

### Instruction 12: Sll
- **Type**: R-TYPE
- **Specification**: Shift left logical `r2` by `r3` (3 bits).
- **Encoding**: `0000000|r2|r3|001|r11|0110011`

### Instruction 13: Srl
- **Type**: R-TYPE
- **Specification**: Shift right logical `r5` by `r3` (3 bits).
- **Encoding**: `0000000|r5|r3|101|r12|0110011`

