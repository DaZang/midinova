#install raspbian

#alsa driver
sudo apt-get install libasound2-de

#libjack-dev
sudo apt-get install libjack-dev

#use python3 for pip
python3 -m pip install --upgrade --force pip#

#python rtmidi
pip install python-rtmidi

#In IDE Thonny use alternative python interpreter: usr/bin/python3

# jackd needed for using ultranova4linux
sudo apt-get install jackd

# needed for building ultranova4linux
sudo apt-get install libboost-dev
sudo apt-get install libusb-1.0-0-dev
sudo apt-get install liblo-dev

mkdir projects
git clone https://github.com/hansfbaier/ultranova4linux.git
# in src/main.cpp change
#define LEN_IN_BUFFER 32
# to 
#define LEN_IN_BUFFER 64
# in Makefile change LIBS = `pkg-config --libs jack libusb-1.0 liblo` -lrt -lboost_system