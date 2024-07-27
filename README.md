HC05 BLUETOOTH-STM32-TRANSCEIVERS-TFT-TOUCH-ILI9341-SPI-TOUCH-STM32F103-STM32F401-
HC05 BLUETOOTH STM32 TRANSCEIVERS TFT TOUCH ILI9341 SPI TOUCH STM32F103 STM32F401

https://www.youtube.com/watch?v=86cz5q3KWE8

![bluetooth stm32 HC05](https://github.com/offpic/BLUETOOTH-STM32-TRANSCEIVERS-TFT-TOUCH-ILI9341-SPI-TOUCH-STM32F103-STM32F401-/assets/31142397/52a56dbf-b7dd-4cd4-aa1b-3117369c2f20)

*****HOW MASTER SLAVE HC05*****

Then we need to run the Serial Monitor and there select “Both NL and CR”, as well as, “38400 baud” rate which is the default baud rate of the Bluetooth module. Now we are ready to send commands and their format is as following.

![73cf26c8b32818b6254a55340260e1c5](https://github.com/offpic/BLUETOOTH-STM32-TRANSCEIVERS-TFT-TOUCH-ILI9341-SPI-TOUCH-STM32F103-STM32F401-/assets/31142397/5200497d-3243-4722-aabd-61af0c3fa76e)



**Master Configuration**

The required AT commands to set the configuration:

1- AT+RMAAD (To clear any paired devices)

2- AT+ROLE=1 (To set it as master)

3- AT+CMODE=0 (To connect the module to the specified Bluetooth address and this Bluetooth address can be specified by the binding command)

4- AT+BIND=xxxx,xx,xxxxxx (Now, type AT+BIND=98d3,31,3069b0 obviously with your respective address to the slave. Note the commas instead of colons given by the slave module.

5- AT+UART=115200,0,0 (To fix the baud rate at 115200)

![Master-Configuration-HC-05-Bluetooth-Module-Arduino](https://github.com/offpic/BLUETOOTH-STM32-TRANSCEIVERS-TFT-TOUCH-ILI9341-SPI-TOUCH-STM32F103-STM32F401-/assets/31142397/8b745a0e-7ceb-48e4-92c8-992e5d74c8ed)



**Slave Configuration**

The required AT commands to set the configuration

1- AT+RMAAD (To clear any paired devices)

2- AT+ROLE=0 (To set it as slave)

3- AT+ADDR (To get the address of this HC-05, remember to jot the address down as it will be used during master configuration)

4- AT+UART=115200,0,0 (To fix the baud rate at 115200)

![Slave-Configuration-HC-05-Bluetooth-Module-Arduino](https://github.com/offpic/BLUETOOTH-STM32-TRANSCEIVERS-TFT-TOUCH-ILI9341-SPI-TOUCH-STM32F103-STM32F401-/assets/31142397/be9d2aac-3492-49cf-b0b1-85ee51dd6c2c)


