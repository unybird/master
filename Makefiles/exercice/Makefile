EXE=hello
OBJ = main.o t1.o stubs.o t2.o

all:$(EXE)

$(EXE) : $(OBJ)
	arm-none-eabi-gcc -L/opt/mylibs -mthumb main.o t1.o stubs.o t2.o -lm -o $@

stubs.o : libs/stubs.c
	arm-none-eabi-gcc -g -O2 -mthumb -c -o $@ $^

t2.o : t2.c
	arm-none-eabi-gcc -Wall -Werror -g -O2 -mthumb -c -o $@ $^

t1.o : t1.c
	arm-none-eabi-gcc -Wall -Werror -g -O2 -mthumb -c -o $@ $^

main.o : main.c
	arm-none-eabi-gcc -Wall -Werror -g -O2 -mthumb -c -o $@ $^


clean : 		
	rm -f hello stubs.o t2.o t1.o main.o

.PHONY : clean allhihi