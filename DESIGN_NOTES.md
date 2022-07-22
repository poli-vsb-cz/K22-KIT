# Signály

Jednoduché zapojení: reference v FRDM-KL02Z a FRDM-KL28Z
- liší se to softwarově od složitějšího zapojení? tzn. používá se v SW signál SDA_RX_EN na pinu
- signály: UART_RX, UART_TX, SPI0_SCK, SPI0_SIN, SPI0_SOUT, SDA_SWD_EN, SDA_SWD_OE, SDA_RST
- PTD4 - LED
- PTD5, PTD6, PTD7 ?!?!?!?!?!

# Užitečné odkazy

- https://github.com/pyocd/FlashAlgo
- https://github.com/ARMmbed/DAPLink/blob/main/docs/PORT_TARGET_FAMILY.md (A flash algorithm blob is needed to program the target MCUs internal (or external) flash memory. This blob contains position independent functions for erasing, reading and writing to the flash controller. Flash algorithm blobs are created from the FlashAlgo project.. An example blob is shown below and would be added to source/family/<mfg>/<targetname>/flash_blob.c)
