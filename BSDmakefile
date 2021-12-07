# Universidade Federal do Rio de Janeiro
# Escola Politecnica
# Departamento de Eletronica e de Computacao
# EEL270 - Computacao II - Turma 2021/2
# Prof. Marcelo Luiz Drumond Lanza
# Autor: <nome completo>
# Descricao: Arquivo de dependencias para FreeBSD

# $Author$
# $Date$
# $Log$

OS = `uname -s`

CC = gcc

.ifdef CLANG
CC = clang
.endif

LD = $(CC)

DIALETO = ansi
STANDARD = -ansi

.ifdef C89
DIALETO = c89
STANDARD = -std=c89
#.elif C90
#DIALETO = c90
#STANDARD = -std=c90
.elif C99
DIALETO = c99
STANDARD = -std=c99
.elif C11
DIALETO = c11
STANDARD = -std=c11
.endif

CFLAGS = -Wall $(STANDARD)
LFLAGS = -Wall

# Roteiro 1 \/ -------------------------------------------------------------------------------------

AULA01 = aula0101 aula0102 aula0103
AULA0101OBJS = aula0101.o
AULA0102OBJS = aula0102.o
AULA0103OBJS = aula0103.o

EXECS = aula0101\
		aula0102\
		aula0103

LIBS =

ALL = $(EXECS) $(LIBS)

# Regra Implicita
.c.o:
	$(CC) $(CFLAGS) -c $<

all: $(ALL)

# Roteiro 1 \/ -------------------------------------------------------------------------------------

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
