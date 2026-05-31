\# RTOS Learning Labs



\## Environment



\- FreeRTOS

\- QEMU LM3S6965

\- ARM GNU Toolchain



\## Completed Labs



\### Lab01 Task Scheduling



\- xTaskCreate()

\- vTaskDelay()



\### Lab02 Task Priority



\- Preemptive scheduling



\### Lab03 Queue Basic



\- Producer Consumer



\### Lab04 Queue Full / Queue Empty



\- Queue blocking

\- Producer Consumer synchronization



\# RTOS Learning Labs



\## Prerequisites



This repository contains only the RTOS lab projects and does not contain the complete FreeRTOS source tree.



Before building any lab, install:



\* QEMU

\* ARM GNU Toolchain

\* CMake

\* Ninja



Download and extract the official FreeRTOS source code.



Expected directory structure:



C:\\RTOS

│

├── FreeRTOS

│   └── FreeRTOS

│       ├── Source

│       └── Demo

│

└── RTOS-Learning\\



---



\## Clone Repository



```powershell

git clone https://github.com/prashantsharana/RTOS-Learning.git

```



Repository structure:



RTOS-Learning

│

├── Lab04\_QueueFull

├── Lab05\_LoggerTask

└── README.md



---



\## Building a Lab



The lab folders cannot be built directly because they depend on the FreeRTOS source tree.



For example, to run Lab05 Logger Task:



1\. Copy all files from:



RTOS-Learning\\Lab05\_LoggerTask



to:



C:\\RTOS\\FreeRTOS\\FreeRTOS\\Demo\\CORTEX\_LM3S6965\_GCC\_QEMU



2\. Open PowerShell:



```powershell

cd C:\\RTOS\\FreeRTOS\\FreeRTOS\\Demo\\CORTEX\_LM3S6965\_GCC\_QEMU

```



3\. Configure:



```powershell

cmake --preset debug

```



4\. Build:



```powershell

cmake --build build

```



5\. Run:



```powershell

qemu-system-arm -machine lm3s6965evb -kernel .\\build\\RTOSDemo.elf -nographic

```



---



\## Available Labs



\### Lab04\_QueueFull



Concepts:



\* Queue Creation

\* Queue Full

\* Queue Empty

\* Producer Consumer Pattern



Tag:



Lab04\_QueueFull



---



\### Lab05\_LoggerTask



Concepts:



\* Gatekeeper Task

\* Logger Queue

\* Shared Resource Protection

\* UART Ownership



Tag:



Lab05\_LoggerTask



