CC ?= gcc

EXE = count
OBJ = count.o lexer.o
LDLIBS = -lfl

all:$(EXE)

$(EXE) : $(OBJ)

count.o: %.o : %.c %.h

clean:
	rm -f $(OBJ) lexer.c $(EXE)

.PHONY: clean all
