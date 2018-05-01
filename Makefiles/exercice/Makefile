CC = arm-none-eabi-gcc

EXE=hello
OBJS = main.o t1.o t2.o stubs.o

all:$(EXE)

$(EXE) : $(OBJS)
	$(CC) -L/opt/mylibs -mthumb main.o t1.o stubs.o t2.o -lm -o $@

stubs.o : libs/stubs.c
	$(CC) -g -O2 -mthumb -c -o $@ $^

t2.o : t2.c
	$(CC) -Wall -Werror -g -O2 -mthumb -c -o $@ $^

t1.o : t1.c
	$(CC) -Wall -Werror -g -O2 -mthumb -c -o $@ $^

main.o : main.c
	$(CC) -Wall -Werror -g -O2 -mthumb -c -o $@ $^


clean : 		
	rm -f hello stubs.o t2.o t1.o main.o

.PHONY : clean all