
.PHONY: clean

all: xwinwrap

xwinwrap: xwinwrap.c
	gcc -Wall -Wstrict-prototypes -Wmissing-prototypes -Wmissing-declarations -Wredundant-decls -lX11 -lXext -lXrender xwinwrap.c -o xwinwrap

install:
	cp xwinwrap /usr/bin

clean:
	rm -f xwinwrap


