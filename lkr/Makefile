CC = cc
CFLAGS = -O2 -Wall
PREFIX = /usr/local

stm8mu_lkr: main.c lang.c linker.c
	$(CC) $(CFLAGS) -I../common -o stm8mu_lkr main.c lang.c linker.c ../common/*.c

install:
	strip stm8mu_lkr
	cp stm8mu_lkr ${PREFIX}/bin/stm8mu_lkr

clean:
	rm -f stm8mu_lkr *~
