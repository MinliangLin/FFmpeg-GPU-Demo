# reference: https://seisman.github.io/how-to-write-makefile/overview.html
CC      = gcc
CFLAGS  = -g -I.
RM      = rm -f
DEPS = foo.h
OBJS = main.o foo.o

default: main

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

main: $(OBJS)
	$(CC) -o $@ $^ $(CFLAGS)

clean:
	$(RM) main