
# 🖥️ RISC-V Reference SoC Tapeout Program (VSD)

## 📌 Introduction
This document provides step-by-step instructions to install essential FPGA design and verification tools(Yosys,Iverilog and gtkwqave) on a Ubuntu Linux system. 

## 🎯 Objective
The purpose of this document is to guide users through the **installation and setup of essential FPGA design and verification tools** on a Linux system.  

By the end of this setup, users will have a working environment to:  
- Perform **HDL design** and **RTL development**  
- Conduct **simulation and functional verification**  
- Analyze **waveforms** using GTKWave  
- Enable efficient **FPGA and ASIC development workflows**
---

### 🔧 The tools covered include:
- **Yosys** 🟢 – An open-source synthesis tool for Verilog  
- **Icarus Verilog (Iverilog)** 🔵 – A Verilog simulation and synthesis tool  
- **GTKWave** 🟣 – A waveform viewer for simulation output  

These tools together create a **complete HDL design and verification environment**.

---

## ⚙️ Before Installing the Tools, Check These Requirements

### 🖥️ System Requirements
To ensure smooth installation and operation of FPGA design and verification tools, your system should meet the following minimum specifications: 
- 💾 **RAM:** 6 GB or more – required for compiling and simulating large HDL designs efficiently  
- 📂 **Storage:** At least 50 GB HDD – to store tools, libraries, and simulation files  
- 🐧 **Operating System:** Ubuntu 20.04 or higher – for compatibility with all tools  
- ⚡ **CPU:** 4 vCPUs or more – to speed up synthesis, simulation, and waveform processing  

---

### **TOOL CHECK  & Installation**

#### <ins>**Yosys**</ins>
```bash
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make               # If make is not installed
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
# Yosys build depends on a Git submodule called abc, which hasn't been initialized yet. You need to run the following command before running make
$ git submodule update --init --recursive
$ make 
$ sudo make install
```
✅ **Yosys installation completed successfully**

<img width="1366" height="768" alt="Yosys Installed" src="https://github.com/user-attachments/assets/6f12972e-ac46-4a1e-ae35-a4e973e395f9" />


#### <ins>**Iverilog**</ins>
```bash
$ sudo apt-get update
$ sudo apt-get install iverilog
```
✅ **Iverilog installation completed successfully**

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/b4541ceb-a38a-4ff1-b125-43d9b4754d7c" />

#### <ins>**gtkwave**</ins>
```bash
$ sudo apt-get update
$ sudo apt install gtkwave
```
✅ **GTKWave installation completed successfully**

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/c211c90e-fb4c-4ad8-8121-d9719ed87410" />


### **CONCLUSION**

- The installation of Yosys, Icarus Verilog, and GTKWave has been successfully completed.
- With this setup, you now have a comprehensive environment for:
      - HDL design
      - RTL synthesis
      - Functional simulation
      - Waveform analysis

This environment enables efficient FPGA and ASIC development workflows. 🚀
Waveform analysis
