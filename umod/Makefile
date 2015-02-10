OBJS=dwcqos_drv.o
OBJS1=dwcqos_dev.o
INCL=dwcqos.h dwcqos_reg.h dwcqos_common.h dwcqos_dev.h
AVBLIB=libdwcqos_drv.a

all: $(AVBLIB)

$(AVBLIB):$(OBJS) $(OBJS1)
	rm -f $@
	ar -cvq $@ $(OBJS) $(OBJS1)

$(OBJS): dwcqos_drv.c $(INCL)
	gcc -c dwcqos_drv.c

$(OBJS1): dwcqos_dev.c $(INCL)
	gcc -c dwcqos_dev.c

clean:
	rm -f `find . -name "*~" -o -name "*.[oa]" -o -name "\#*\#" -o -name TAGS -o -name core -o -name "*.orig"`
