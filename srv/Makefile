NAME=srv
SRC=$(NAME).c

CFLAG =-std=gnu99 -O0 -Wall -g -pipe -D_GNU_SOURCE -D_REENTERANT -I/usr/include
LIBS=-ljansson -lpthread -ldl

MACHINE := $(shell uname -m)

ifeq ($(MACHINE), x86_64)
	LIBDIR = /usr/lib64
else
	LIBDIR = /usr/lib
endif

$(NAME):
	gcc -o $(NAME) $(SRC) $(CFLAG) -L$(LIBDIR) $(LIBS)
	strip $(NAME)
clean:
	rm -f $(NAME)


