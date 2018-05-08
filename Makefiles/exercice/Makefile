CC = arm-none-eabi-gcc

EXE = hello
OBJS = main.o t1.o t2.o stubs.o
CFLAGS =-Wall -Werror -g -O2
LDLIBS = -L/opt/mylibs -lm
TARGET_ARCH = -mthumb
vpath %.c = libs/

all:$(EXE)

$(EXE) : $(OBJS)
	$(LINK.o) $^ $(LDLIBS) -o $@

%.o : %.c %.h 

stubs.o : CFLAGS = -g -O2

clean : 		
	rm -f hello stubs.o t2.o t1.o main.o

.PHONY : clean all