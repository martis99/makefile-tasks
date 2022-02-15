CC:=gcc
CFLAGS:=-Wall
LIB:=calculator.so

PREFIX:=/usr

.PHONY: clean all install uninstall

all: $(LIB)

$(LIB): math_functions.c
	$(CC) $(CFLAGS) -fpic -shared -o $(LIB) $^

install: $(LIB)
	install -d $(PREFIX)/lib $(PREFIX)/include
	install -m 555 $(LIB) $(PREFIX)/lib
	install -m 644 math_functions.h $(PREFIX)/include

uninstall:
	$(RM) $(PREFIX)/lib/$(LIB)
	$(RM) $(PREFIC)/include/math_functions.h

clean:
	$(RM) $(LIB) *.o
