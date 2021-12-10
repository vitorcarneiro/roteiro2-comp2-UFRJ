# Universidade Federal do Rio de Janeiro
# Escola Politecnica
# Departamento de Eletronica e de Computacao
# EEL270 - Computacao II - Turma 2021/2
# Prof. Marcelo Luiz Drumond Lanza
# Autor: <nome completo>
# Descricao: Arquivo de dependencias para Linux

# $Author$
# $Date$
# $Log$

OS = $(shell uname -s)

CC = gcc

ifeq ($(cc), CLANG)
CC = clang
endif

LD = $(CC)

DIALETO = ansi
STANDARD = -ansi

ifeq ($(dialeto), C89)
DIALETO = c89
STANDARD = -std=c89
endif

ifeq ($(dialeto), C90)
DIALETO = c90
STANDARD = -std=c90
endif

ifeq ($(dialeto), C99)
DIALETO = c99
STANDARD = -std=c99
endif

ifeq ($(dialeto), C11)
DIALETO = c11
STANDARD = -std=c11
endif

CFLAGS = -Wall $(STANDARD)
LFLAGS = -Wall

# \/ OBJS MACROS\/ --------------------------------------------------------------------------------
# -- Roteiro 1 \/ ---------------------------------------------------------------------------------
AULA01 = aula0101 aula0102 aula0103
AULA0101OBJS = aula0101.o
AULA0102OBJS = aula0102.o
AULA0103OBJS = aula0103.o
# -- Roteiro 1 /\ ---------------------------------------------------------------------------------

# -- Roteiro 2 \/ ---------------------------------------------------------------------------------
AULA02 = aula0202a aula0202b aula0202c aula0202d
AULA0202AOBJS = aula0201a.o aula0202.o
AULA0202BOBJS = aula0201b.o aula0202.o
AULA0202COBJS = aula0201c.o aula0202.o
AULA0202DOBJS = aula0201d.o aula0202.o
# -- Roteiro 2 /\ ---------------------------------------------------------------------------------
# /\ OBJS MACROS/\ --------------------------------------------------------------------------------


# \/ LIBS MACROS\/ --------------------------------------------------------------------------------
# -- Roteiro 2 \/ ---------------------------------------------------------------------------------
LIBMATEMATICARECURSAOOBJS = aula0201a.o
LIBMATEMATICADOWHILEOBJS = aula0201b.o
LIBMATEMATICAFOROBJS = aula0201c.o
LIBMATEMATICAWHILEOBJS = aula0201d.o
# -- Roteiro 2 /\ ---------------------------------------------------------------------------------
# /\ LIBS MACROS/\ --------------------------------------------------------------------------------



EXECS = aula0101\
		aula0102\
		aula0103\
		aula0202a\
		aula0202b\
		aula0202c\
		aula0202d

LIBS =	libmatematicarecursao.a\
	libmatematicadowhile.a\
	libmatematicafor.a\
	libmatematicawhile.a\
	libmonitor.a\
	libbase.a

ALL = $(EXECS) $(LIBS)

# Regra Implicita
.c.o:
	$(CC) $(CFLAGS) -c $<

all: $(ALL)

# -- Roteiro 1 \/ ----------------------------------------------------------------------------------
aula01: $(AULA01)

aula0101: $(AULA0101OBJS)
	$(LD) $(LFLAGS) -o $@ $(AULA0101OBJS)
	cp -f $@ $@-$(OS)-$(CC)-$(DIALETO)

aula0102: $(AULA0102OBJS)
	$(LD) $(LFLAGS) -o $@ $(AULA0102OBJS)
	cp -f $@ $@-$(OS)-$(CC)-$(DIALETO)

aula0103: $(AULA0103OBJS)
	$(LD) $(LFLAGS) -o $@ $(AULA0103OBJS)
	cp -f $@ $@-$(OS)-$(CC)-$(DIALETO)
# -- Roteiro 1 /\ ---------------------------------------------------------------------------------


# -- Roteiro 2 \/ ----------------------------------------------------------------------------------
aula02: $(AULA02)

aula0202a: $(AULA0202AOBJS)
	$(LD) $(LFLAGS) -o $@ $(AULA0202AOBJS)
	cp -f $@ $@-$(OS)-$(CC)-$(DIALETO)

aula0202b: $(AULA0202BOBJS)
	$(LD) $(LFLAGS) -o $@ $(AULA0202BOBJS)
	cp -f $@ $@-$(OS)-$(CC)-$(DIALETO)

aula0202c: $(AULA0202COBJS)
	$(LD) $(LFLAGS) -o $@ $(AULA0202COBJS)
	cp -f $@ $@-$(OS)-$(CC)-$(DIALETO)

aula0202d: $(AULA0202DOBJS)
	$(LD) $(LFLAGS) -o $@ $(AULA0202DOBJS)
	cp -f $@ $@-$(OS)-$(CC)-$(DIALETO)

libmatematicarecursao.a: $(LIBMATEMATICARECURSAOOBJS)
	ar -r -c $@ $(LIBMATEMATICARECURSAOOBJS)

libmatematicadowhile.a: $(LIBMATEMATICADOWHILEOBJS)
	ar -r -c $@ $(LIBMATEMATICADOWHILEOBJS)

libmatematicafor.a: $(LIBMATEMATICAFOROBJS)
	ar -r -c $@ $(LIBMATEMATICAFOROBJS)

libmatematicawhile.a: $(LIBMATEMATICAWHILEOBJS)
	ar -r -c $@ $(LIBMATEMATICAWHILEOBJS)
# -- Roteiro 2 /\ ---------------------------------------------------------------------------------



.PHONY: clean clean-all clean-objs clean-freebsd clean-linux clean-gcc clean-clang clean-ansi clean-c89 clean-c90 clean-c99 clean-c11

clean:
	rm -f *.o $(ALL) *.core

clean-all:
	rm -f *.o $(ALL) *-FreeBSD-* *-Linux-* *.core

clean-objs:
	rm -f *.o *.core

clean-freebsd:
	rm -f *.o $(ALL) *-FreeBSD-* *.core

clean-linux:
	rm -f *.o $(ALL) *-Linux-* *.core

clean-gcc:
	rm -f *.o $(ALL) *-gcc-* *.core

clean-clang:
	rm -f *.o $(ALL) *-clang-* *.core

clean-ansi:
	rm -f *.o $(ALL) *-ansi *.core

clean-c89:
	rm -f *.o $(ALL) *-c89 *.core

#clean-c90:
#	rm -f *.o $(ALL) *-c90 *.core

clean-c99:
	rm -f *.o $(ALL) *-c99 *.core

clean-c11:
	rm -f *.o $(ALL) *-c11 *.core

# $RCSfile$
