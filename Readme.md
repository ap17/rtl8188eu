rtl8188eu ( idVendor=0bda, idProduct=8179 ) driver v5.3.9_28540.20180627

origin : https://github.com/aircrack-ng/rtl8188eus

Currently (march 2020) used by me on Xunlong Orange OPi H3 and H5 with Linux 5.6, Debian 10. Works great both in access point mode and in infrastructure mode.

This driver must be built in "in-tree" mode.

1.    put driver sources to ".../drivers/net/wireless/realtek/rtl8188eu"
2.    into file ".../drivers/net/wireless/realtek/Kconfig" insert line:

source "/drivers/net/wireless/realtek/rtl8188eu/Kconfig"

3.    into file ".../drivers/net/wireless/realtek/Makefile" insert line:

obj-$(CONFIG_RTL8188EU) += rtl8188eu/

4.    do : make menuconfig -> device drivers-> network device support -> wireless LAN -> select 8188eu
5.    do make.
