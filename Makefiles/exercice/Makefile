CC = arm-none-eabi-gcc

EXE = hello
SOURCES = t1.c t2.c stubs.c
OBJS = main.o $(SOURCES:%.c=%.o)
CFLAGS =-Wall -Werror -g -O2
LDFLAGS = -L/opt/mylibs
LDLIBS = -lm
TARGET_ARCH = -mthumb
vpath %.c = libs/

-include $(subst .c,.d,$(SOURCES))

all:$(EXE)

$(EXE) : $(OBJS)
	$(LINK.o) $^ $(LDLIBS) -o $@

%.o : %.c %.h 

stubs.o : CFLAGS = -g -O2

clean : 		
	rm -f $(EXE) $(OBJS)

.PHONY : clean all