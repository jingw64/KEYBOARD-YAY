# Microcontroller!

Date: May 20, 2026
Authors: Jingyuan Wen, Richard Ding

## What is a microcontroller?

[What is a microcontroller? | IBM](https://www.ibm.com/think/topics/microcontroller)

A microcontroller is basically a small computer you can program, but less complicated than your actual computer. It’s composed of:

- **CPU:** The “brain”, also called a microprocessor
- **Memory:** RAM and EEPROM
  - RAM (random access memory) is lost if the system loses power, used for temporary data during run time (volatile memory)
  - EEPROM (electrically erasable programmable read-only memory), or flash memory, holds the programs and instruction set (wtf is ISA)
  - Flash memory is non-volatile, and should only be altered when we “flash” (program) the microcontroller
- **Peripherals:** Other components that can speak with the microcontroller
  - I/O (input output) interfaces: timers, counters, ADC and DAC
  - Communication protocols: SPI, I2C, UART, CAN—used for communicating with screens, sensors, and other interfaces

While both can appear in the shape of a single chip, the main difference between the microcontroller and a microprocessor is the existence of memory and peripherals.

## Microcontrollers to Consider

| **Chips** | **Link** |
| --- | --- |
| ATMega32u4 | [AliExpress - ATMega32u4](https://www.aliexpress.us/w/wholesale-atmega32u4-microcontroller.html?spm=a2g0o.home.search.0) |
| RP2040 | [AliExpress - RP2040](https://www.aliexpress.us/w/wholesale-rp2040-microcontroller.html?spm=a2g0o.home.search.0) |
| nRF52840 | [AliExpress - nRF52840](https://www.aliexpress.us/w/wholesale-nrf52840-microcontroller.html?spm=a2g0o.home.search.0) |
| ESP32 | [AliExpress - ESP32](https://www.aliexpress.us/w/wholesale-esp32-microcontroller.html?spm=a2g0o.home.search.0) |
| STM32 | [AliExpress - STM32](https://www.aliexpress.us/w/wholesale-stm32-microcontroller.html?spm=a2g0o.home.search.0) |

---

### 1. ATMega32u4

Uses: Runs classic wired keyboards. Runs QMK or VIA.

Pros:

- Native hardware USB support
- Compatible with many firmwares
- Reliability

Cons:

- Kind of old
- Low memory (32KB)

---

### 2. RP2040

Uses: Often found in keyboards that require higher performances, split keyboards, and keyboards that have complicated RGB matrices. Runs QMK/VIA/KMK.

Pros:

- Very affordable
- Lots of memory (2MB-16MB external flash)
- Programmable I/O blocks
- Sub-processors that can mimic other hardware to relieve stress from main CPU

Cons:

- No built-in wireless capabilities
- High power consumption

---

### 3. nRF52840

Uses: Low power bluetooth keyboards. Runs ZMK firmware.

Pros:

- Power efficiency (batteries can last months on a single charge)
- Bluetooth and USB
- ZMK firmware (the go-to for wireless keyboards).

Cons:

- Boards that use it are a bit expensive
- A bit of a learning curve to break into

---

### 4. ESP32

Uses: Wireless keyboards that requires Wi-Fi.

Pros:

- Integrated Wi-Fi + Bluetooth,
- Very cheap for good performance.
- Can create an ecosystem for general IoT programming for future projects.

Cons:

- High power consumption, as Wi-Fi drains battery (built-in battery necessary).
- USB support varies (ESP32 lacks native USB, but ESP32-S2/S3 has it, though keyboard firmware support is less seamless than RP2040).

---

### 5. STM32

Uses: High end keyboards that require a lot of pins and fast processing.

Pros:

- Lots of chips tailored to specific needs (pin count, speed)
- Native USB support for most models
- Industry standard for embedded systems

Cons:

- Lots of variants
- Will need to work with complex registers and specialized IDEs due to configuration

---
  