# Makefile for 'input' module

CC=gcc
CCFLAGS=-Wall
CLEAN=rm -rf *.o
OBJ=lexer.o inp.o chem.o basis.o interactive.o qslex.o

lexer.o: lexer.c
	$(CC) $(CCFLAGS) -c lexer.c -o lexer.o

qslex.o: qslex.c
	$(CC) $(CCFLAGS) -c qslex.c -o qslex.o

interactive.o: interactive.c
	$(CC) $(CCFLAGS) -c interactive.c -o interactive.o

inp.o: inp.c
	$(CC) $(CCFLAGS) -fopenmp -c inp.c -o inp.o

chem.o: chem.c
	$(CC) $(CCFLAGS) -c chem.c -o chem.o

basis.o: basis.c
	$(CC) $(CCFLAGS) -c basis.c -o basis.o
	
input.o: $(OBJ)
	ld -r $(OBJ) -o input.o

clean:
	$(CLEAN)
