ASM = ../../asm/stm8mu_asm

ASM_OPTIONS += -I
ASM_OPTIONS += -DTEST0=256

syntax.l0: syntax.asm
	$(ASM) $(ASM_OPTIONS) syntax.asm

clean:
	rm -f *.l0 *~
