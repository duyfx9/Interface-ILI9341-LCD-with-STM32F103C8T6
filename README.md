# Interface-ILI9341-LCD-with-STM32F103C8T6
a small example to communicate between LCD ILI9341 and STM32F103C8T6

1.Introduce

This is how to interface ILI9341 LCD with STM32F103C8T6 using STM32CubeIDE.
I added 2 new fonts with larger sizes
You can take a look at my repository to see how to print letters and numbers to the screen using printf 
https://github.com/duyfx9/TFT_Clock

2.Schematic

ILI9341    STM32	
VCC	      3.3V
GND 	    G	
CS	      B10			
RESET	    B1		
DC	      B0	
MOSI	    A7
SCK	      A5
LED	      3.3V

3.Setup

System Core → RCC → HSE → Crytal/Creamic Resonator
Clock Config → 72MHz

Setup SPI
Connectivity → SPI 1 → Mode : Transmit only master
Parameter Setting → Prescaler (for Baud rate) →4
DMA Setting → Add →SPI1_TX
Set PB0 PB1 PB10 is GPIO_Output

Add library
Core → Inc → New flie 
add 3 file .h 
Core → Src → New flie 
add 3 file .c
add include and some code i leave in Example →ILI_9341_STM_32_F103 → Src → main.c


4.Reference
https://www.micropeta.com/video37
https://www.youtube.com/watch?v=8hypVJ2U7OE
