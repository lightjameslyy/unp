include ../Make.defines

SRCS = $(wildcard *.c)

OBJS = $(patsubst %.c, %.o, $(SRCS))

TARGETS = $(patsubst %.c, %.bin, $(SRCS))

%.o: %.c
	${CC} ${CFLAGS} -c $< -o $@

%.bin: %.o
	${CC} ${CFLAGS} -o $@ $^ ${LIBS}

all: $(TARGETS)

clean:
		rm -f ${TARGETS} ${CLEANFILES}
