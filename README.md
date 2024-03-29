# VSDSquadron-Mini-RISC-V-Research-Internship

# VSDSquadron_MINIRISC-V

To learn more about the VSDSquadron Mini RISC-V internship projects, you have come to the right place. You will receive all the tools need to gain hands-on expertise with Mini RISC-V throughout the four weeks of this internship. Enjoy your educational experience!!

VSDSQUADRON Mini Board 

![VSDSQUADRON Mini Board]()

BOARD SPECS:

| CH32V003F4U6 chip with 32-bit RISC-V core based on RV32EC instruction set |
| ------------------------------------------------------------------------- 
| SRAM                                                                       2kb onchip volatile sram     16kb external program memory                                    |
| Processor                                                                  24 MHz                                                                                       |
| Sink Current per I/O Pin                                                   8 mA                                                                                         |
| Source Current per I/O Pin                                                 8 mA                                                                                         |
| Input voltage (nominal)                                                    5 V                                                                                          |
| I/O voltage                                                                3.3 V                                                                                        |
| Programmer/debugger                                                        Onboard RISC-V programmer/debugger, USB to TTL serial port support                           |
| SPI                                                                        1x, PC5(SCK), PC1(NSS), PC6(MOSI), PC7(MISO)                                                 |
| I2C                                                                        1x, PC1(SDA), PC2(SCL)                                                                       |
| USART                                                                      1x, PD6(RX), PD5(TX)              



### The first online meet was held on 16th of Feb 2024 @6PM

<details>
    <summary> TASK 1 </summary>

1) install RISC-V GNU Toolchain 

2) install Yosys 

3) install iverilog 

4) install gtkwave

### CLONING RISC-V GNU TOOLCHAIN

Step-1

```sudo apt install git-all```   # To install git

![To install git](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/gnu_img1.png)
![To install git](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/gnu_img2.png)

```sudo apt-get install autoconf automake autotools-dev curl python3 libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev``` *make sure to install the dependencies*

![To install dependencies](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/gnu_img3.png)
![To install dependencies](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/gnu_img4.png)

```git clone https://github.com/riscv/riscv-gnu-toolchain```

![gnu_toolchain_clone](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/gnu_img5.png)


## Create a opt dir
```mkdir /opt/riscv```  *try sudo incase of permission denial*

In my case I created a driectory ```mkdir riscv``` and ``` chmod 777 home/vanshikatanwar/riscv ```

## Config and make inside the risc-v gnu toolchain dir 

```./configure --prefix=/opt/riscv```  

In my case ```./configure --prefix=/home/vanshikatanwar/riscv``` 

![gnu_toolchain_clone](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/gnu_img6.png)

![gnu_toolchain_clone](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/gnu_img7.png)


Then
```make``` **(Have patience)**
![gnu_toolchain_clone](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/gnu_img8.png)

### 2. Installing YOSYS
 ```git clone https://github.com/YosysHQ/yosys.git```
 
 ```cd yosys```
 
 ```make --version command```
![yosys_img1](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img1.png)
 
 ```
    sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
```


![yosys_img2](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img2.png)
![yosys_img3](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img3.png)
![yosys_img4](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img4.png)
![yosys_img5](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img5.png)

```
$ make config-gcc
```

![yosys_img2](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img6.png)
![yosys_img3](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img7.png)

```
$ make 
$ sudo make install
```

![yosys_img4](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img8.png)
![yosys_img5](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img9.png)
![yosys_img4](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img10.png)
![yosys_img5](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img11.png)
![yosys_img4](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/yosys_img12.png)



### 3. Installing iVerilog

```sudo apt-get install iverilog```

![iverilog](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/iverilog_img1.png)

### 4. Installing GTKwave

```sudo apt update```

```
sudo apt install gtkwave
```

![gtkwave](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/gtkwave_img1.png)


<details>
    <summary> TASK 2 </summary>

--> To Determine that identify the instruction type and to also find out the exact 32 bit instruction code, based on it's instruction type. 

### Instruction type

There are 6 Instruction Formats . These are :- 

(i) R-Type Format or R-Type Instruction - This type of instruction includes registers. These instructions are basically using 3 register inputs , - add,xor, mul.etc. (Basically, it's contains all arithmetic and logic operations).

(ii) I-Format or I-Type Instruction - These are the instructions with immediates , loads like, 
-addi, lw, jalr, slli.

(iii) S-Format or S-Type Instruction
(iv) SB-Format or SB-Type Instruction
(v) U-Format or U-Type Instruction
(vi) UJ-Format or UJ-Type Instruction


In this internship, we are proceeding with R-type Instruction.
As, ISA type is RISC-V in VSDSQUADRON Board.

This R-Type Instruction is 32-bit Long and have the following formats.
--> This 32bit long format are containing total of 2 bits, and these bits are divided into some parts .
These parts are known as fields. Hence, this 32 bit is containing some fields . And to define these fileds, it contains following bit of numbers. 

These are, 755357.
Each bit , which is mentioned above have some meaning , in 32-bit format. 
7+5+5+3+5+7=32.

7- Funct7
5- rs2
5- rs1
3- Funct3
5- rd
7- opcode

![R-type Instruction Format](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/r-type%20instruction%20format.png)


Here, 5-bit fields can represent numbers 0-31, i.e., (2^5=32)
while, 7-bit fields can represent numbers 0-128, i.e., (2^7=128) and similarly so on for other bits.






The initial section in the R-type instruction format is referred to as the opcode field, which can also be called the operation code. This 7-bit opcode (bits 0-6) indicates the instruction format type, like R-type, I-type, U-type and so on. The opcode describes which instruction format is being used.

The next part in the R-type instruction format is referred to as the rd field. Rd in the "rd field" means Destination Register. This rd field shows where the result of the operation is kept. The length of the rd field is 5 bits (7-11).

The funct3 field comes after the destination register and is 3 bits long, spanning from bit 12 to bit 14. This field provides information about the type of operation being performed, such as whether it is addition, subtraction, or some other logical operation. The purpose of the funct3 field is to encode the operation so the processor knows what type of action to take on the data. While the overall text structure flows from describing the location of the field, to its length, and then its purpose, the key ideas have been reworded to avoid simply repeating the original phrasing.


There are two registers called rs1 and rs2, each 5 bits long. Rs1 spans bits 15-19 and rs2 spans bits 20-24.

The funct7 field is the last field in the R-type instruction format. It specifies the operation type, like shift or multiply. Both the funct3 and funct7 fields describe the operation, depending on the instruction format.

So , if one will conclude it now for the instruction which we are going to execute during this learning is 
Add r6,r1,r2.
Now, if we compare it with the 32 bit instruction format ...
It means that ,
r6 --> Rd (destination register) 
r1--> rs1. (source register 1)[input 1]
r2--> rs2(source register 2) [input 2]


r6=r1+r2
ie., rd=rs1+rs2















<details>
    <summary> TASK 3 </summary>


Performing C based lab.

C code sum of no. 1 to n 

`
#include<stdio.h>
int main() {
  int sum=0, i=1, n=100;
  for(i = 1; i <= n; ++i){
    sum += 1;
  }
  printf("Sum of numbers from 1 to %d is %d \n",n,sum);
  return 0;
}`




![gcc compiler ss](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/IMG-20240227-WA0001.jpg)





![gcc compiler ss](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/IMG-20240227-WA0005.jpg)



![gcc compiler ss](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/IMG_20240227_171202.jpg)




<details>
    <summary> TASK 4 </summary>
    observation with -O1 and -Ofast. Upload snapshot of compiled C Code, RISC-V Objdmp

    
![task4 ss1](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task3-ss1.png)

![task4 ss2](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task3-ss2.png)

![task4 ss2.1](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task3-ss2.1.png)

![task4 ss2.2](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task3-ss2.2.png)

![task4 ss3](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task3-ss3.png)




<details>
    <summary> TASK 5 </summary>

To simulate and run the Verilog code, enter the following commands in your terminal.


`

![task5_verilog_simulation](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task%205%2001.png)




To see the output waveform in gtkwave, enter the following commands in your terminal.




![task5_verilog_simulation2](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task_5_gtkwave%201.png)


![task5_verilog_simulation3](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task_5_gtkwave%202.png)

Add Operation 
![task5_verilog_simulation4](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task%205%2002.png)

![task5_verilog_simulation5](https://github.com/VanshikaTanwar/VSDSquadron-Mini-RISC-V-Research-Internship-/blob/main/IMG/task%205%2003%20.png)


## References

- [References]()
- 


...

