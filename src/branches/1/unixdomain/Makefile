VERSION =
EXE = unixstrserv01$(VERSION)
objects = $(EXE).o unp.o readline.o wraplib.o wrapstdio.o wrapunix.o wrapsock.o error.o signal.o
CC = gcc
CFLAGS = -Wall -g

$(EXE):$(objects)
	$(CC) $(CFLAGS) -o $(EXE) $(objects)
	
$(EXE).o:$(EXE)$(VERSION).c
	$(CC) $(CFLAGS) -c $(EXE)$(VERSION).c -I ../lib

unp.o:../lib/unp.c ../lib/unp.h
	$(CC) $(CFLAGS) -c ../lib/unp.c

readline.o:../lib/readline.c ../lib/unp.h
	$(CC) $(CFLAGS) -c ../lib/readline.c

wraplib.o:../lib/wraplib.c ../lib/unp.h
	$(CC) $(CFLAGS) -c ../lib/wraplib.c

wrapstdio.o:../lib/wrapstdio.c ../lib/unp.h
	$(CC) $(CFLAGS) -c ../lib/wrapstdio.c

wrapunix.o:../lib/wrapunix.c ../lib/unp.h
	$(CC) $(CFLAGS) -c ../lib/wrapunix.c

wrapsock.o:../lib/wrapsock.c ../lib/unp.h
	$(CC) $(CFLAGS) -c ../lib/wrapsock.c

error.o:../lib/error.c ../lib/unp.h
	$(CC) $(CFLAGS) -c ../lib/error.c
	
signal.o:../lib/signal.c ../lib/unp.h
	$(CC) $(CFLAGS) -c ../lib/signal.c
