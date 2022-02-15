compiler:=gcc
Flags:=-Wall -I.
OBJS:=main.o math_functions.o
BIN:=calculator

all: $(BIN)

$(BIN): main.o math_functions.o
	$(compiler) $(Flags) -o $(BIN) main.o math_functions.o
	
main.o: main.c
	$(compiler) $(Flags) -c main.c
	
math_functions.o: math_functions.c math_functions.h
	$(compiler) $(Flags) -c math_functions.c
	
clean:
	rm -f $(BIN) $(OBJS)