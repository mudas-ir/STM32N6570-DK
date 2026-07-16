# STM32N6570-DK

In this file im writing, so far what i have done in STM32N6570-DK board

## Getting started with STM32N6570-DK

## Links

1.  Preloaded Demo programe (STM32N6-OOB) Only hex file is avalable, Example Projects & Demo Projects for Peripherals 
    (STM32CubeN6) are [Link_1](https://www.st.com/en/embedded-software/stm32cuben6.html#get-software).

2.  Edge AI Projects are [here](https://www.st.com/en/development-tools/stm32n6-ai.html#get-software).

3.  ST provides an official "build an AI application from scratch on the STM32N6570-DK" tutorial that walks through creating an AI project,configuring the software,
    and deploying a model. It's an excellent companion once you've learned the fundamentals.

    STM32N6570-DK AI application tutorial :
    https://community.st.com/stm32-mcus-60/how-to-build-an-ai-application-from-scratch-on-the-stm32n6570-dk-using-stm32cubemx-154895?utm_source=chatgpt.com

4.  There's also official support for the board in Edge Impulse if you later want to experiment with end-to-end data collection, model training, and deployment without
    building the entire pipeline yourself.

    Edge Impulse STM32N6570-DK documentation :
    https://docs.edgeimpulse.com/hardware/boards/stm32n6570-dk?utm_source=chatgpt.com

5.  For an overview of the hardware and ST's recommended workflow, this webinar is also useful:
    https://www.youtube.com/watch?v=u1bDyDm961g

## The following software and versions I used:

| Software              | Version |
|-----------------------|---------|
| STM32CubeIDE          | 1.17.0  |
| STM32CubeMX           | 6.17.0  |
| STM32CubeProgrammer   | 2.18.0  |
| STM32Cube_FW_N6       | 1.4.0   |
| Edge AI Projects      | 2.1.1   |

## How to Flash the Example Projects into the external flash

These Example Projects i have downloaded from [Link_1]



# Getting Started with STM32N6570-DK

This document summarizes my progress while learning and experimenting with the **STM32N6570-DK** development board. It includes useful resources, software versions, and notes on flashing example projects.

---

## Resources

### 1. Preloaded Demo Program (STM32N6-OOB)

The STM32N6570-DK board comes with the **STM32N6-OOB** (Out-of-Box) demo preloaded in the external flash.

- Only the HEX file is available.
- Example projects and peripheral demo projects are available in **STM32Cube_FW_N6**.

**Download:** `Link_1`

---

### 2. Edge AI Projects

The official Edge AI example projects are available here:

**Download:** `Link_2`

---

### 3. Official AI Application Tutorial

ST provides an excellent step-by-step tutorial for building an AI application from scratch on the STM32N6570-DK. It covers:

- Creating a new project
- Configuring STM32CubeMX
- Integrating AI models
- Building and deploying the application

https://community.st.com/stm32-mcus-60/how-to-build-an-ai-application-from-scratch-on-the-stm32n6570-dk-using-stm32cubemx-154895

---

### 4. Edge Impulse Support

The STM32N6570-DK is officially supported by Edge Impulse, making it easy to:

- Collect data
- Train AI models
- Deploy models to the board

Documentation:

https://docs.edgeimpulse.com/hardware/boards/stm32n6570-dk

---

### 5. Webinar

For an overview of the hardware and ST's recommended development workflow:

https://www.youtube.com/watch?v=u1bDyDm961g

---

## Software Versions

The following software versions were used during development:

| Software              | Version |
|-----------------------|---------|
| STM32CubeIDE          | 1.17.0  |
| STM32CubeMX           | 6.17.0  |
| STM32CubeProgrammer   | 2.18.0  |
| STM32Cube_FW_N6       | 1.4.0   |
| Edge AI Projects      | 2.1.1   |

---

# Flashing Example Projects to External Flash

The example projects were downloaded from **Link_1**.

This section describes how to program the example projects into the external flash memory of the STM32N6570-DK board.

> *(Add the flashing procedure here.)*

Example:

1. Open **STM32CubeProgrammer**.
2. Connect the board via ST-LINK.
3. Select the external flash loader.
4. Load the generated `.hex` or `.bin` file.
5. Program the external flash.
6. Reset the board to run the application.

---

## Notes

This README is a collection of notes and instructions gathered while learning the STM32N6570-DK platform. It will be updated as I explore more features, peripherals, and Edge AI applications.
