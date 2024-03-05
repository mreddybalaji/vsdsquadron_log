
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


![image](https://github.com/mreddybalaji/vsdsquadron_log/assets/130784457/892ae43e-9dae-4f22-ba72-6dd7950d6d96)


```

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

