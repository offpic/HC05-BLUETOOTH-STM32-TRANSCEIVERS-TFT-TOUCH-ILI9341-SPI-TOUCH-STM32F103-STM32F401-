# BLUETOOTH-STM32-TRANSCEIVERS-TFT-TOUCH-ILI9341-SPI-TOUCH-STM32F103-STM32F401-
BLUETOOTH STM32 TRANSCEIVERS TFT TOUCH ILI9341 SPI TOUCH STM32F103 STM32F401 

![bluetooth stm32 HC05](https://github.com/offpic/BLUETOOTH-STM32-TRANSCEIVERS-TFT-TOUCH-ILI9341-SPI-TOUCH-STM32F103-STM32F401-/assets/31142397/52a56dbf-b7dd-4cd4-aa1b-3117369c2f20)

*****HOW MASTER SLAVE HC05*****
![73cf26c8b32818b6254a55340260e1c5](https://github.com/offpic/BLUETOOTH-STM32-TRANSCEIVERS-TFT-TOUCH-ILI9341-SPI-TOUCH-STM32F103-STM32F401-/assets/31142397/d9367ecc-1661-4cdb-b48f-b039147d6c8d)



*Master Configuration*

The required AT commands to set the configuration:

1- AT+RMAAD (To clear any paired devices)

2- AT+ROLE=1 (To set it as master)

3- AT+CMODE=0 (To connect the module to the specified Bluetooth address and this Bluetooth address can be specified by the binding command)

4- AT+BIND=xxxx,xx,xxxxxx (Now, type AT+BIND=98d3,34,906554 obviously with your respective address to the slave. Note the commas instead of colons given by the slave module.

5- AT+UART=115200,0,0 (To fix the baud rate at 115200)



*Slave Configuration*

The required AT commands to set the configuration

1- AT+RMAAD (To clear any paired devices)

2- AT+ROLE=0 (To set it as slave)

3- AT+ADDR (To get the address of this HC-05, remember to jot the address down as it will be used during master configuration)

4- AT+UART=115200,0,0 (To fix the baud rate at 115200)


