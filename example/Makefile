obj-m += lkm_example.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

test: all
	-sudo rmmod lkm_example
	sudo dmesg -C
	sudo insmod lkm_example.ko
	dmesg

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean
