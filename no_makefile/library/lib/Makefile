CC:=gcc
CFLAGS:=-Wall
LIB:=libfile_reader.so

PREFIX:=/usr

.PHONY: clean all install uninstall

all: $(LIB)

$(LIB): file_reader.o
	$(CC) $(CFLAGS) -fpic -shared -o $@ $^

file_reader.o: file_reader.c file_reader.h
	$(CC) $(CFLAGS) -c -o $@ $<

install:
	install -d $(PREFIX)/lib $(PREFIX)/include
	install -m 555 $(LIB) $(PREFIX)/lib
	install -m 644 file_reader.h $(PREFIX)/include

uninstall:
	$(RM) $(PREFIX)/lib/$(LIB)
	$(RM) $(PREFIX)/include/file_reader.h

clean:
	$(RM) $(LIB) *.o