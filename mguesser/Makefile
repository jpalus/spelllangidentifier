CFLAGS=-Wall -g -O2 -DUDM_GUESSER_STANDALONE -DLMDIR=\"./maps\" -DMGUESSER_VERSION=\"0.4\"
LIBS=-lm
CC=cc


all: mguesser


mguesser: guesser.o crc32.o utils.o Makefile
	$(CC) $(CFLAGS) guesser.o crc32.o utils.o -o mguesser $(LIBS)


guesser.o: guesser.c
	$(CC) $(CFLAGS) -c guesser.c

crc32.o: crc32.c
	$(CC) $(CFLAGS) -c crc32.c

utils.o: utils.c
	$(CC) $(CFLAGS) -c utils.c


clean:
	rm -f mguesser *.o
