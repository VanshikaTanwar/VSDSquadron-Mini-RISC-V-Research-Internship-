# VSDSquadron-Mini-RISC-V-Research-Internship

# VSDSquadron_MINIRISC-V

To learn more about the VSDSquadron Mini RISC-V internship projects, you have come to the right place. You will receive all the tools need to gain hands-on expertise with Mini RISC-V throughout the four weeks of this internship. Enjoy your educational experience!!

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

```sudo apt install git-all```   # To install git

```sudo apt-get install autoconf automake autotools-dev curl python3 libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev``` *make sure to install the dependencies*

![gnu_dependencies](https://github.com/Nawras-Ahamed/VSD_Squadron_mini_Research/assets/50738659/3a354063-2d87-44c5-8b54-e2f13d2b1965)

```git clone https://github.com/riscv/riscv-gnu-toolchain```

![gnu_toolchain_clone](https://github.com/Nawras-Ahamed/VSD_Squadron_mini_Research/assets/50738659/760e3e42-8c07-4254-80a3-050e489ac42d)


## Create a opt dir
```mkdir /opt/riscv```  *try sudo incase of permission denial*

In my case I created a driectory ```mkdir riscv``` and ``` chmod 777 home/nawras/riscv ```

## Config and make inside the risc-v gnu toolchain dir 

```./configure --prefix=/opt/riscv```  

In my case ```./configure --prefix=/home/nawras/riscv```  

Then
```make``` **(Have patience)**
|
| External interrupts                                                        8 external interrupt edge detectors, but it only maps one external interrupt to 18 I/O ports |
| PWM pins                                                                   14X                                                                                          |
| Analog I/O pins                                                            10-bit ADC, PD0-PD7, PA1, PA2, PC4                                                           |
| Digital I/O pins                                                           15                                                                                           |
| Built-in LED Pin                                                           1X onboard user led (PD6)                                                                    |
| USB 2.0 Type-C                                                            

