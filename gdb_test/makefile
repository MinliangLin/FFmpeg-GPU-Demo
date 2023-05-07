# reference: https://seisman.github.io/how-to-write-makefile/overview.html
CC      = gcc
CFLAGS  = -g -fPIC -I.
RM      = rm -f
DEPS = foo.h
OBJS = main.o foo.so

default: main.out

main.out: $(OBJS)
	$(CC) -o $@ $^ $(CFLAGS)

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

foo.so: foo.o
	$(CC) -shared -o $@ $< $(CFLAGS)

clean:
	$(RM) main.out
