# STM32N6570-DK

## Getting started with STM32N6570-DK

This document summarizes my progress while learning and experimenting with the **STM32N6570-DK** development board. It includes useful resources, software versions, and 
notes on flashing example projects.
---

## Resources

### Links

#### 1. Example Projects 

- The STM32N6570-DK board comes with the **STM32N6-OOB** (Out-of-Box) demo preloaded in the external flash (Only the HEX file is available).
- Example projects and peripheral demo projects are available in **STM32Cube_FW_N6**.

**Download:** [Link_1](https://www.st.com/en/embedded-software/stm32cuben6.html)

---

#### 2. Edge AI Projects

The official Edge AI example projects are available here:

**Download:** [Link_2](https://www.st.com/en/development-tools/stm32n6-ai.html#get-software)

---

#### 3. Official AI Application Tutorial

ST provides an excellent step-by-step tutorial for building an AI application from scratch on the STM32N6570-DK. It covers:

- Creating a new project
- Configuring STM32CubeMX
- Integrating AI models
- Building and deploying the application

STM32N6570-DK AI application tutorial link : [Link_3](https://community.st.com/stm32-mcus-60/how-to-build-an-ai-application-from-scratch-on-the-stm32n6570-dk-using-stm32cubemx-154895?utm_source=chatgpt.com)

---

#### 4. Webinar

For an overview of the hardware and ST's recommended development workflow: [Link_4](https://www.youtube.com/watch?v=u1bDyDm961g)

---

## The following software and versions I used:

| Software              | Version |
|-----------------------|---------|
| STM32CubeIDE          | 1.17.0  |
| STM32CubeMX           | 6.17.0  |
| STM32CubeProgrammer   | 2.18.0  |
| STM32Cube_FW_N6       | 1.4.0   |
| Edge AI Projects      | 2.1.1   |

---

## Boot Modes

The STM32N6 series does not have internal flash memory. To retain firmware after a reboot, program it into the external flash. Alternatively, you can load firmware directly into SRAM (development mode), but note that the program will be lost if the board is powered off in this mode.

Development Mode: used for loading firmware into RAM during a debug session or for programming firmware into external flash.

Boot from Flash: used to boot firmware from external flash.

|                  | STM32N6570-DK                                                                | NUCLEO-N657X0-Q                                                                  |
| -------------    | -------------                                                                |-----------------                                                                 |
| Boot from flash  | ![STM32N6570-DK Boot from flash](_htmresc/STM32N6570-DK_Boot_from_flash.png) | ![NUCLEO-N657X0-Q Boot from flash](_htmresc/NUCLEO-N657X0-Q_Boot_from_flash.png) |
| Development mode | ![STM32N6570-DK Development mode](_htmresc/STM32N6570-DK_Dev_mode.png)       | ![NUCLEO-N657X0-Q Development mode](_htmresc/NUCLEO-N657X0-Q_Dev_mode.png)       |

---

## How to dump program into External Flash 

### Example Projects

The example projects were downloaded from [Link_1](#1-example-projects).

This section describes how to program the example projects into the external flash memory of the STM32N6570-DK board.

1. Download the STM32Cube_FW_N6 from the above link.
2. Navigate to the project path `STM32Cube_FW_N6_V1.4.0\Projects\STM32N6570-DK\Examples`.
3. The `Example` folder includes n number of individual projects, select any one, as of now im going with GPIO.
4. Navigate to the `Examples\GPIO\GPIO_IOToggle\STM32CubeIDE` and open this `STM32CubeIDE` folder using STM32CubeIDE as shown below.
5. Open STM32CubeIDE, Click -> File -> Open Project from File System.
6. Right click the GPIO_IOToggle_FSBL (in FSBL), goto Properties -> C/C++ Build -> Settings -> Build Steps.
7. Under Post-build steps -> Command: , past the below command and Click Apply and Close
 ```
 cd "${ProjDirPath}/Debug" && echo y | "C:\Program Files\STMicroelectronics\STM32Cube\STM32CubeProgrammer\bin\STM32_SigningTool_CLI.exe" -bin "${ProjName}.bin" -nk -of 0x80000000 -t fsbl -o "${ProjName}-Trusted.bin" -hv 2.3 -dump "${ProjName}-Trusted.bin"
 ```
8. Now we can build the project.
9. After the build is completed, a `.bin` file is created in the following path `GPIO\GPIO_IOToggle\STM32CubeIDE\FSBL\Debug` by the name `GPIO_IOToggle_FSBL-Trusted.bin`
10. Open STM32CubeProgrammer
11. 

---

## Notes

This README is a collection of notes and instructions gathered while learning the STM32N6570-DK platform. It will be updated as I explore more features, peripherals, 
and Edge AI applications.
