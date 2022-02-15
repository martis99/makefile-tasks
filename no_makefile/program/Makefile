CC:=gcc
CFLAGS:=-Wall -I.
BINS:=calculator

all: $(BINS)

$(BINS): main.o maths.o usage.o
	$(CC) $(CFLAGS) -o $@ $^
	
main.o: main.c
	$(CC) $(CFLAGS) -c main.c
	
maths.o: maths.c maths.h
	$(CC) $(CFLAGS) -c maths.c
	
usage.o: usage.c usage.h
	$(CC) $(CFLAGS) -c usage.c

clean:
	rm -f $(BINS) *.o