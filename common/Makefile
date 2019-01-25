#
# Makefile
#

TARGET = libcommon.a

CFLAGS += -I. -Wall

libcommon_obj := \
	btorder.o \
	llist.o \
	token.o \
	memdata.o \
	stm8chip.o \
	debug.o \
	memdata.o \
	srec.o \
	bmem.o \
	l0.o \
	symbol.o \
	section.o \
	relocation.o \
	lang_constexpr.o \
	lang_util.o

.PHONY: all clean

.c.o:
	${CC} ${CFLAGS} -c -o $@ $<

all: $(TARGET)

clean:
	rm -f $(TARGET) ${libcommon_obj} *~

$(TARGET): ${libcommon_obj}
	$(AR) r $@ ${libcommon_obj}
