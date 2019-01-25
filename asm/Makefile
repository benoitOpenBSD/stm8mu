CC = cc
CFLAGS = -O2 -Wall
PREFIX = /usr/local

stm8mu_asm: main.c assembler.c lang.c lang_instruction.c
	$(CC) $(CFLAGS) -I../common -o stm8mu_asm main.c assembler.c lang.c lang_instruction.c ../common/libcommon.a

install:
	strip stm8mu_asm
	cp stm8mu_asm ${PREFIX}/bin/stm8mu_asm

clean:
	rm -f stm8mu_asm *~
