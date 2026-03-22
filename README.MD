\# HW2 Q1 - Hello World (PS Only)



\## Overview

Simple Hello World application running on the Zynq PS (ARM Cortex-A9) without any PL bitstream.

Demonstrates the basic Vivado + Vitis embedded flow.



\## Requirements

\- Zybo Z7-10 board

\- Vivado 2025.2

\- Vitis 2025.2



\## Hardware Setup

1\. Connect Zybo Z7-10 via USB

2\. Set boot mode jumper to JTAG



\## Steps to Run



\### Vivado

1\. Open `edt\_zybo.xpr` in Vivado

2\. No bitstream needed — just export hardware:

&nbsp;  - File → Export → Export Hardware → Pre-synthesis → Finish



\### Vitis

1\. Open Vitis → New Workspace

2\. File → New Component → Platform

&nbsp;  - Point to `system\_wrapper.xsa`

&nbsp;  - Processor: `ps7\_cortexa9\_0`, Standalone

3\. Build platform

4\. File → New Component → Application → Examples → Hello World

5\. Build application

6\. Open serial terminal (COM4, 115200 baud)

7\. Click Run



\## Expected Output

```

Hello World

Successfully ran Hello World application

```



\## Notes

\- No bitstream required — PS runs independently of PL

\- UART baud rate: 115200

