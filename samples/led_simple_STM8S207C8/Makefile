ASM = ../../asm/stm8mu_asm
LINKER = ../../lkr/stm8mu_lkr
FLASH = ../../flash/stm8mu_flash

ASM_OPTIONS += -I
LINKER_OPTIONS += -M -MD
LINKER_OPTIONS += -p --script=led.lkr 
LINKER_OPTIONS += --output=led.s19 --s19head="Test LED"

FLASH_CHIP = STM8S207C8
FLASH_BAUD = 115200
FLASH_CPORT = /dev/ttyU0

led.l0: led.asm
	$(ASM) $(ASM_OPTIONS) led.asm

led.s19: led.l0
	$(LINKER) $(LINKER_OPTIONS) led.l0 >led.map

flash: led.s19
	$(FLASH) --chip=$(FLASH_CHIP) --baud=$(FLASH_BAUD) --cport=$(FLASH_CPORT) --input=$^ write

all: led.s19

clean:
	rm -f *.l0 *~ *.s19 *.map
