CC=gcc -O2 -g -Wall -Werror -std=c99
prefix=/usr
executable=fibo
%.o: %.c
		$(CC) -c $< -o $@

all: fibo

fibo: fibo.o
		$(CC) -o $(executable) fibo.o -static -lgmp

install: fibo
		install -m 0755 $(executable) $(prefix)/bin

.PHONY: install

clean:
		rm -f *.o $(executable)
