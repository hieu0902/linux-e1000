# SPDX-License-Identifier: GPL-2.0
# Copyright(c) 1999 - 2006 Intel Corporation.

#
# Makefile for the Intel(R) PRO/1000 ethernet driver
#

obj-$(CONFIG_E1000) += e1000.o
e1000-objs := e1000_main.o e1000_hw.o e1000_ethtool.o e1000_param.o

export KROOT=/lib/modules/$(shell uname -r)/build

allofit:  modules
modules:
	@$(MAKE) -C $(KROOT) M=$(PWD) modules
modules_install:
	@$(MAKE) -C $(KROOT) M=$(PWD) modules_install
kernel_clean:
	@$(MAKE) -C $(KROOT) M=$(PWD) clean

clean: kernel_clean
	rm -rf   Module.symvers modules.order

