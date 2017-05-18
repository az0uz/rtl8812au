## RTL8812AU driver for Raspberry Pi supporting monitor mode and frame injection
This repo is a fork from https://github.com/marczis/rtl8812au branch v.4.3.21

To build on your Raspberry pi:

update to the last supported kernel:
```bash
sudo apt-get install rpi-update
sudo rpi-update
```

install raspberrypi/linux source to compile the driver:
```bash
sudo wget https://raw.githubusercontent.com/notro/rpi-source/master/rpi-source -O /usr/bin/rpi-source && sudo chmod +x /usr/bin/rpi-source && /usr/bin/rpi-source -q --tag-update
rpi-source
```

download/build/install this driver:
```bash
sudo apt-get install git build-essential
git clone https://github.com/az0uz/rtl8812au
cd rtl8812au
make -j4
sudo make install
```

you can delete the linux source in your home folder afterward as it takes a lot of space
