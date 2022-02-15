CC:=gcc
CFLAGS:=-Wall
CPPFLAGS:=-I.
OBJS:=main.o maths.o usage.o
BIN:=calculator

PREFIX:=/usr

.PHONY: clean all install uninstall

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) -o $@ $^

main.o: main.c
	$(CC) $(CFLAGS) $(CPPFLAGS) -c -o $@ $<
	
maths.o: maths.c maths.h
	$(CC) $(CFLAGS) $(CPPFLAGS) -c -o $@ $<
	
usage.o: usage.c usage.h
	$(CC) $(CFLAGS) $(CPPFLAGS) -c -o $@ $<

install:
	install -d $(PREFIX)/bin
	install -m 555 $(BIN) $(PREFIX)/bin

uninstall:
	$(RM) $(PREFIX)/bin/$(BIN)

clean:
	$(RM) $(BIN) $(OBJS)