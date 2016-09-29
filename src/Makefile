export KDIR ?= /lib/modules/`uname -r`/build

# Compiler Flags
ccflags-y := -Wall -Werror -I$(M)/../include -I$(M)/../include/linux_kernel

# Build the OpenXT framebuffer module.
obj-m += xengnttab.o
xengnttab-objs := gntshr_core.o gnttab_core.o

all: modules

modules:
	$(MAKE) -C $(KDIR) M=$(shell pwd)

modules_install: 
	$(MAKE) -C $(KDIR) M=$(shell pwd) modules_install
