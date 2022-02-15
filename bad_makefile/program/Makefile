CC:=gcc
CFLAGS:=-Wall
CPPFLAGS:=-I.
OBJS:=main.o math_functions.o
BIN:=calculator

PREFIX:=/usr

.PHONY: clean all install uninstall

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) -o $@ $^
	
main.o: main.c
	$(CC) $(CFLAGS) $(CPPFLAGS) -c -o $@ $^
	
math_functions.o: math_functions.c math_functions.h
	$(CC) $(CFLAGS) $(CPPFLAGS) -c -o $@ $<

install:
	install -d $(PREFIX)/bin
	install -m 555 $(BIN) $(PREFIX)/bin

uninstall:
	$(RM) $(PREFIX)/bin/$(BIN)

clean:
	$(RM) $(BIN) $(OBJS)