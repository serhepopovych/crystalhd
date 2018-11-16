
ifneq ($(KERNELRELEASE),)
include Kbuild
else
# normal makefile
KERNELDIR ?= /lib/modules/$(shell uname -r)/build

all: clean modules

modules:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules
clean:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) clean
endif
