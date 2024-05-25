## I. Introduction 

This is how to interface _ILI9341 LCD_ with _STM32F103C8T6_ using _STM32CubeIDE_

You can take a look at _my repository_ to see how to print letters and numbers to the screen using printf [github_link](https://github.com/duyfx9/TFT_Clock)

## II. Schematic

|ILI9341  | STM32 |
|:-------:|:-----:|
| VCC     | 3.3V  |
| GND     | G     |
| CS      | B10   |
| RESET   | B1    |
| DC      | B0    |
| MOSI    | A7    |
| SCK     | A5    |
| LED     | 3.3V  |

## III. Set up

### 1. Set up RCC
- **Step 1**. System Core → RCC → HSE → Crytal/Creamic Resonator
- **Step 2**. Clock Config → 72MHz
 
### 2. Set up SPI
- **Step 1**.Connectivity → SPI 1 → Mode : Transmit only master

- **Step 2**.Parameter Setting → Prescaler (for Baud rate) → 4

- **Step 3**.DMA Setting → Add → SPI1_TX

- **Step 4**.Set PB0 PB1 PB10 is GPIO_Output

- **Step 5**.Add library

    - Core → Inc → New flie 
    - Add 3 file .h 
    - Core → Src → New flie 
    - Add 3 file .c
    - Add include and some code i leave in Example →ILI_9341_STM_32_F103 → Src → main.c


## IV. References
https://www.micropeta.com/video37
https://www.youtube.com/watch?v=8hypVJ2U7OE





