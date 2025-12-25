# STM32 Bare-Metal Drivers

A collection of **MCAL-level drivers** for the STM32F103 (Blue Pill)
implemented in pure **Bare-Metal C** using the STM32 Reference Manual.

## Philosophy
No HAL. No CubeMX.
Every bit written intentionally.

## Drivers Overview

### RCC Driver
- Reads clock configuration registers
- Calculates SYSCLK, HCLK, PCLK1, PCLK2
- Handles prescalers and clock sources

### GPIO Driver
- Pin configuration (Input / Output / AF)
- Pull-up / Pull-down support

### USART Driver
- Polling & Interrupt modes
- Configurable data size, parity, stop bits
- Baud rate calculation without floating point
## File Structure
Drivers/
├── Stm32_F103C6_Drivers/
│ ├── RCC/
│ │ └── RCC.c / RCC.h
│ ├── GPIO/
│ │ └── GPIO.c / GPIO.h
│ ├── USART/
│ │ └── USART.c / USART.h
│ └── EXTI/
│ └── EXTI.c / EXTI.h
├── src/
│ │ └── main.c
├── HAL/
│ ├── KEYPAD_DRIVER/
│ │ └── KEYPAD.c / KEYPAD.h
│ ├── LCD_DRIVER/
│ │ └── LCD.c / LCD.h
│ ├── Seven_Segment_DRIVER/
│ │ └── Seven_Segment.c / Seven_Segment.h

## Getting Started
  ### Requirements
    - STM32F103C6 (Blue Pill)
    - ARM GCC Toolchain or STM32CubeIDE
    - USB to Serial adapter (if using USART debugging)
    - ST-Link programmer (for flashing)

    
## Contributing
1. Fork the repo
2. Create a new branch
3. Commit changes
4. Open a Pull Request

## License
MIT License
