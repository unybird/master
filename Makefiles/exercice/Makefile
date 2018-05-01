hello : main.o t1.o stubs.o t2.o
	arm-none-eabi-gcc -L/opt/mylibs -mthumb main.o t1.o stubs.o t2.o -lm -o hello

stubs.o : libs/stubs.c
	arm-none-eabi-gcc -g -O2 -mthumb -c -o stubs.o libs/stubs.c

t2.o : t2.c
	arm-none-eabi-gcc -Wall -Werror -g -O2 -mthumb -c -o t2.o t2.c

t1.o : t1.c
	arm-none-eabi-gcc -Wall -Werror -g -O2 -mthumb -c -o t1.o t1.c

main.o : main.c
	arm-none-eabi-gcc -Wall -Werror -g -O2 -mthumb -c -o main.o main.c


clean : 		
	rm -f hello stubs.o t2.o t1.o main.o

.PHONY : clean all