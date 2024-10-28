# MifareClassic-worktime-reader
Basic worktime reader project based on Raspberry Pico (RP2040) written in C with my own driver for PN532 based on PN532 docs. It is using SPI and IRQ line to communicate between Raspberry Pico and PN532. It supports only Mifare Classic cards but allows to protect them with key A. Cards will contain number of scans to add extra protection from cloned cards that can cause mismatch in scan number on Raspberry Pico and Mifare Card.

This project also contains simple driver for 2 line LCD connected to Raspberry Pico through I2C with PCF8574 expander.

In order to add new card or delete card (from dictionary based on modulo hashing table) you have to use admin card that is hardcoded in worktime_device.c main function and input card on PN532 reader.

Simple connections diagram:
![obraz](https://github.com/user-attachments/assets/3fa13621-bf57-4db5-879c-c8b964f22ee3)


