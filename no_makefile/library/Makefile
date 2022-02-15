CC:=gcc
CFLAGS:=-Wall
BINS:=file_reader.so calculator

all: $(BINS)

calculator: main.c
	$(CC) $(CFLAGS) -o $@ $^ -L. file_reader.so

file_reader.o: file_reader.c file_reader.h
	$(CC) $(CFLAGS) -o $@ -c file_reader.c

file_reader.so: file_reader.o
	$(CC) $(CFLAGS) -o $@ -shared file_reader.o

clean:
	rm -f $(BINS) *.o