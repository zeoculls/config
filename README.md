# config


Disable NetworkManager:
https://myridia.com/dev_posts/view/2022

To disable Network Manager on Debian 8 or later:
$ sudo systemctl stop NetworkManager.service
$ sudo systemctl disable NetworkManager.service


To enable it, make the following change in the Makefile:

CONFIG_PLATFORM_I386_PC = y
CONFIG_PLATFORM_ARM_RPI = n
to

CONFIG_PLATFORM_I386_PC = n
CONFIG_PLATFORM_ARM_RPI = y

Testing de SD Card performance:

curl https://raw.githubusercontent.com/geerlingguy/raspberry-pi-dramble/master/setup/benchmarks/microsd-benchmarks.sh | sudo bash
