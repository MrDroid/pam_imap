
CC=gcc
CFLAGS=-g -O2 -fPIC  -I.. -I /usr/kerberos/include
DEFINE=-DHAVE_CONFIG_H
LDFLAGS=
LIBS=-lz -lnsl  -lcrypto -lcrypt -lpam_misc -lssl
#CFLAGS=-Wall -O -g -Wno-deprecated -Wshadow -Wmissing-prototypes -I. -I..
#LFLAGS=-lssl -lcrypto -lnsl -ldb -L/lib
#DEFINE=-DHAVE_CONFIG_H -DHAVE_LIBSSL -DDEBUG

#PROG=imaptest
#OBJ=imaptest.o imap.o sync.o config.o maildir.o list.o cram.o dotlock.o
OBJ=config.o imap.o list.o cram.o helpers.o

all: $(OBJ) 

$(PROG): $(OBJ) 
	$(CC) $(CFLAGS) $(LFLAGS) $(LIBS) $(DEFINE) -o $(PROG) $(OBJ) 

imap.o: imap.c
	$(CC) $(CFLAGS) $(DEFINE) -c imap.c

imaptest.o: imaptest.c
	$(CC) $(CFLAGS) $(DEFINE) -c imaptest.c

helpers.o: helpers.c
	$(CC) $(CFLAGS) $(DEFINE) -c helpers.c

maildir.o: maildir.c
	$(CC) $(CFLAGS) $(DEFINE) -c maildir.c

list.o: list.c
	$(CC) $(CFLAGS) $(DEFINE) -c list.c

cram.o: cram.c
	$(CC) $(CFLAGS) $(DEFINE) -c cram.c

dotlock.o: dotlock.c
	$(CC) $(CFLAGS) $(DEFINE) -c dotlock.c

config.o: config.c
	$(CC) $(CFLAGS) $(DEFINE) -c config.c

partial_clean:
	rm -f main.o	
clean:
	rm -f *.o $(PROG) $(OBJ) 
