CC = cc
CFLAGS = -O2 -Wall
PREFIX = /usr/local

stm8mu_flash: main.c cport.c ew.c program.c
	$(CC) $(CFLAGS) -I../common -o stm8mu_flash main.c cport.c ew.c program.c ../common/libcommon.a

install:
	strip stm8mu_flash
	cp stm8mu_lkr ${PREFIX}/bin/stm8mu_flash

clean:
	rm -f stm8mu_flash *~
