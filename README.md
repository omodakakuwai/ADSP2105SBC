## ADSP2105SBC
The ADSP2105SBC is a home-built single board computer equipped with Analog Devices ADSP-2105 DSP in 90s, capable of running home-built VTL interpreter.

Three 8-bit wide EPROMs are used to store 24-bit wide instruction codes.<BR>
16k words external data memory space is allocated as follows.

[0000-2FFF] External SRAM: 12k words (32k bytes SRAM is used)<br>
[3000-37FF] UART: 2k words (only 2 bytes are used for Control/Data Registers)<br>
[3800-39FF] Internal RAM: 512 words (used as pseudo-registers and stack area)<br>
[3A00-3BFF] Reserved: 512words<br>
[3C00-3FFF] Memory-mapped Control Registers: 1k words<br>

ADSP-2105 has a 16-level hardware stack, but it is insufficient to realize multiple subroutine calls in the VTL interpreter,
software stack is implemented by using internal RAM as stack area.

![](https://github.com/omodakakuwai/ADSP2105SBC/blob/main/images/ADSP2105SBC_MAIN.jpg)
![](https://github.com/omodakakuwai/ADSP2105SBC/blob/main/images/ADSP2105SBC_SUB.jpg)
