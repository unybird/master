CC = arm-none-eabi-gcc

EXE = hello
OBJS = main.o t1.o t2.o stubs.o
LOADLIBES = -L/opt/mylibs
CFLAGS = -Wall -Werror -g -O2 -mthumb
LDLIBS = -lm

all:$(EXE)

$(EXE) : $(OBJS)
	$(LINK.o) $(LOADLIBES) -mthumb $^ $(LDLIBS) -o $@

stubs.o : libs/stubs.c
	$(CC) -g -O2 -mthumb -c -o $@ $^

#t2.o : t2.c
#	$(CC) $(CFLAGS) -c -o $@ $^

#t1.o : t1.c
#	$(CC) $(CFLAGS) -c -o $@ $^

#main.o : main.c
#	$(CC) $(CFLAGS) -c -o $@ $^


clean : 		
	rm -f hello stubs.o t2.o t1.o main.o

.PHONY : clean all