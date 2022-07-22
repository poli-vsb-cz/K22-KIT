# Signály

Jednoduché zapojení: reference v FRDM-KL02Z a FRDM-KL28Z
- liší se to softwarově od složitějšího zapojení? tzn. používá se v SW signál SDA_RX_EN na pinu
- signály: UART_RX, UART_TX, SPI0_SCK, SPI0_SIN, SPI0_SOUT, SDA_SWD_EN, SDA_SWD_OE, SDA_RST
- PTD4 - LED
- PTD5, PTD6, PTD7 ?!?!?!?!?!

# Můj seznam signálů (z FRDM-K22)

- PTA0, PTA1, PTA2, PTA3 - SWD/JTAG input
- PTA4 - OpenSDA SWD_EN_B
- PTA18, PTA19 - krystal
- PTB0 - OpenSDA SWD_OE_B
- PTB1 - OpenSDA reset (0 - bootloader, 1 - aplikace; současně je to připojené to HW resetu aplikačního MCU)
- PTC3 - OpenSDA UART1_RX
- PTC4 - OpenSDA UART1_TX
- PTC5, PTC6, PTC7 - OpenSDA SWD output (do aplikačního MCU)
- PTD4 - aplikační tlačítko
- PTD4 - OpenSDA LEDka
- PTD5 - Aplikační LEDka
- PTD5 - OpenSDA 5V USB power sense
- PTD6 - OpenSDA Power enable - asi není potřeba (je to výstup)
- PTD7 - OpenSDA VTRG_FAULT_B
- RESET - pullup do 3V3

# Užitečné odkazy

- https://github.com/pyocd/FlashAlgo
- https://github.com/ARMmbed/DAPLink/blob/main/docs/PORT_TARGET_FAMILY.md (A flash algorithm blob is needed to program the target MCUs internal (or external) flash memory. This blob contains position independent functions for erasing, reading and writing to the flash controller. Flash algorithm blobs are created from the FlashAlgo project.. An example blob is shown below and would be added to source/family/<mfg>/<targetname>/flash_blob.c)
