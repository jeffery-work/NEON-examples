BIN=fft-test
CC=arm-linux-gnueabihf-gcc
CFLAGS= -mthumb -march=armv7-a -mfpu=neon -ffast-math
LIBS=./lib/libNE10.a

INCS=-I./include/ 
SRCS:=$(wildcard *.c ./src/*.c) 
COBJS:=$(SRCS:.c=.o)

all:$(BIN)

$(COBJS) : %.o: %.c
	$(CC) -c $< -o $@ $(INCS) $(CFLAGS)

$(BIN):$(COBJS)
	$(CC) -o $(BIN) $(COBJS) $(LIBS) $(CFLAGS) 

clean:
	rm $(BIN) $(COBJS)
