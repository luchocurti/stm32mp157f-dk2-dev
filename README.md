# STM32MP157F-DK2 Embedded Project

Embedded software development project targeting the **STM32MP157F-DK2 Discovery Kit** by STMicroelectronics, using the Yocto Project and the OpenSTLinux distribution.

## Hardware Platform

| Component | Description |
|---|---|
| Manufacturer | STMicroelectronics |
| Board | STM32MP157F-DK2 Discovery Kit |
| Motherboard | MB1272 |
| Daughterboard | MB1407 |
| MPU | STM32MP157FAC1 |
| Application Processor | Dual Arm Cortex-A7 @ 800 MHz |
| Real-Time Processor | Arm Cortex-M4 @ 209 MHz |
| RAM | 512 MB DDR3L |
| Storage | microSD |
| Wireless | Wi-Fi 802.11 b/g/n |
| Bluetooth | Bluetooth Low Energy 4.1 |

### Processing Architecture

The STM32MP157 integrates two different processing environments:

- **Cortex-A7:** Runs Linux, providing the application environment, networking, filesystem, user-space applications and other operating system services.
- **Cortex-M4:** Runs real-time firmware, providing deterministic execution for time-critical tasks and direct peripheral control.

Both processing environments can communicate through the hardware-supported interprocessor communication mechanisms.

## Software Platform

| Component | Technology |
|---|---|
| Operating System | Linux |
| Build System | Yocto Project |
| Distribution | OpenSTLinux |
| Architecture | ARMv7-A / ARMv7E-M |
| Application Development | C / C++ |
| Real-Time Firmware | STM32CubeMP15 |

## Repository Structure

```text
.
├── assets/
├── docs/
│   ├── board/
│   │   ├── DB4022-Discovery kits STM32MP157 MPUs.pdf
│   │   ├── TN1235-Overview of ST-LINK derivatives.pdf
│   │   ├── UM2637-Discovery kits STM32MP157 MPUs.pdf
│   │   └── UM2909-Getting started with X-LINUX-GNSS1 package.pdf
│   └── microprocessor/
│       └── DS12505-Arm dual Cortex-A7 Cortex-M4 MPU.pdf
├── .gitignore
├── LICENSE
└── README.md
```

### Documentation

The `docs/` directory contains hardware-related documentation.

- `board/`: Board-specific documentation, technical notes and user manuals.
- `microprocessor/`: MPU datasheets and errata.

## ST Software Packages

STMicroelectronics provides three software packages for the STM32MP1 series, each targeting a different development stage:

| Package | Description | Purpose |
|---|---|---|
| **Starter Package** | Provides pre-built Linux images and binaries. | Flash and boot the development board with a ready-to-use Linux distribution. |
| **Developer Package** | Provides an SDK and source code for key BSP components, including the Linux Kernel, U-Boot, and Device Tree. | Develop, debug, and customize low-level software components. |
| **Distribution Package** | Provides the complete OpenEmbedded/Yocto build environment. | Build, customize, and maintain a complete Linux distribution for the target hardware. |

### Package Overview

- **Starter Package:** Get Linux up and running quickly without building the system from source.
- **Developer Package:** Work with the source code of individual software components and develop applications using the provided SDK.
- **Distribution Package:** Build a fully customized Linux distribution using Yocto and OpenEmbedded.

## External Resources

### PC prerequisites

- [PC prerequisites – STMicroelectronics](https://wiki.st.com/stm32mpu/wiki/PC_prerequisites)

### STMicroelectronics

- [Getting Started with the STM32MP1 Starter pack](https://www.st.com/stm32mp1-getting-started)
- [STM32MP157F-DK2 - Discovery kit](https://www.st.com/en/evaluation-tools/stm32mp157f-dk2.html)
- [MB1272 Motherboard](https://wiki.st.com/stm32mpu/wiki/MB1272)
- [MB1407 Daughterboard - 480x800 pixels DSI display](https://wiki.st.com/stm32mpu/wiki/MB1407)
- [STM32MP157F MPU with Arm Dual Cortex](https://www.st.com/en/microcontrollers-microprocessors/stm32mp157f.html)

### STM32MPU Developer Documentation

- [Getting started with STM32MP157x Discovery kit](https://wiki.st.com/stm32mpu/wiki/Getting_started/STM32MP1_boards/STM32MP157x-DK2)
=> - [STM32MP15 Discovery Kits - Starter Package](https://wiki.st.com/stm32mpu/wiki/STM32MP15_Discovery_kits_-_Starter_Package)
    => 12.2. Examples running on Cortex-M4
- [STM32 MPU Wiki](https://wiki.st.com/stm32mpu/wiki/Main_Page)
- [STM32CubeMP15 Package - Getting Started](https://wiki.st.com/stm32mpu/wiki/STM32CubeMP15_Package_-_Getting_started)
- [Getting Started with STM32Cube Ecosystem​](https://dev.st.com/stm32cube-docs/stm32cube-getting-started/latest/en/index.html)
- [STM32MP157x Discovery kit wiki category](https://wiki.st.com/stm32mpu/wiki/Category:STM32MP15_Discovery_kits)

### Tools Installation

- [Tools installation: Install STM32CubeIDE](https://wiki.st.com/stm32mcu/wiki/STM32StepByStep:Step1_Tools_installation#Install_STM32CubeIDE)
- [Tools installation: Install STM32CubeMX](https://wiki.st.com/stm32mcu/wiki/STM32StepByStep:Step1_Tools_installation#Install_STM32CubeMX)
- [Tools installation: Install STM32CubeProgrammer](https://wiki.st.com/stm32mcu/wiki/STM32StepByStep:Step1_Tools_installation#Install_STM32CubeProg)

### Video Tutorials

- [STM32MP1 Tutorials and Getting Started](https://www.youtube.com/playlist?list=PLnMKNibPkDnFeV4sBarnsAtFTg7h6V-9_)

## Development Environment

The development environment is based on Linux and the Yocto Project.

## Subjects to Explore

1. **Linux fundamentals:** Boot process, kernel, root filesystem, systemd.
2. **Yocto:** Build OpenSTLinux, understand BitBake, create your own layer and recipes.
3. **Hardware integration:** Device Tree, GPIO, I2C, SPI, UART.
4. **Kernel development:** Configure, compile and customize the Linux kernel.
5. **Driver development:** Write and integrate your own Linux kernel driver.
6. **Cortex-M4 integration:** Develop firmware and communicate with Linux using RPMsg.
7. **Advanced topics:** Secure boot, OTA updates, networking and system optimization.

## License

See [LICENSE](LICENSE) for details.

--------------------------------------------------------------------------------

How to access the board through the host computer:
    Serial terminal through the USB ST-LINK/V2-1
        minicom -D /dev/ttyACM0
        root@stm32mp1-e1-7e-67:~# 
    SSH connection through Ethernet or Wi-Fi
        ssh root@192.168.1.xxx
        root@stm32mp1-e1-7e-67:~# 

