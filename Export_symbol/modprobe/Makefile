obj-m := avg_mod/avg.o add_mod/add.o
KERNELDIR = /lib/modules/$(shell uname -r)/build/
PWD := $(shell pwd)

default:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules
clean:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) clean
install:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules_install
	depmod -a
