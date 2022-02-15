CC:=gcc
CFLAGS:=-Wall
CPPFLAGS:=-I../lib
LDFLAGS:=-L../lib -lfile_reader
OBJS:=main.o
BIN:=program

PREFIX:=/usr

.PHONY: clean all install uninstall

$(BIN): $(OBJS)
	$(CC) -o $@ $^ $(LDFLAGS)

main.o: main.c
	$(CC) $(CFLAGS) $(CPPFLAGS) -c -o $@ $<

install:
	install -d $(PREFIX)/bin
	install -m 555 $(BIN) $(PREFIX)/bin

uninstall:
	$(RM) $(PREFIX)/bin/$(BIN)

clean:
	$(RM) $(BIN) $(OBJS)