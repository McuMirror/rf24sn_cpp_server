RF24SN C++ Server
=================

Fork from [RF24SN_CPP_Server](https://github.com/VaclavSynacek/RF24SN_CPP_Server).
And patch to match of Raspberry Pi 2, new version of RF24-rpi and libmosquitto 1.4.

## Installation:

Install [RF24-rpi](https://github.com/deaware/RF24-rpi)

Clone all resource

```Shell
git clone https://github.com/deawarehub/RF24SN_CPP_Server.git
cd RF24SN_CPP_Server
```

Install libmosquitto v1.4
```Shell
tar -xvf libmosquitto-1_4.tar.gz
cd libmosquitto-1_4
sudo cp libmosquitto.so.1 /usr/lib
```

Then compile
```Shell
make
```

## Usage:
```Shell
sudo ./RF24SN
```




## Wiring

```Shell
nRF24L01+                  Raspberry Pi 2

GND          <----->       GND
VCC          <----->       +3.3V
CE           <----->       GPIO22 [15]
CSN          <----->       GPIO7 [26]
SCK          <----->       GPIO11 (SPI_CLK) [23]
MOSI         <----->       GPIO10 (SPI_MOSI) [19]
MISO         <----->       GPIO9 (SPI_MISO) [21]
```