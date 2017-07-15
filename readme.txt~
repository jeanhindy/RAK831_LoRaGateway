# Description:
#	Installation procedure for FTDI SPI-over-USB dependencies

-----------------------------------------------------------------------------------------

# [STEP 1] Download and unpack the RAK831_LoRaGateway
# File must match SHA1 Checksum: 1b994a23b118f83144261e3e786c43df74a81cd5
#Method one
wget https://github.com/RAKWiskey/RAK831_LoRaGateway-test/archive/master.zip

unzip master.zip

#Method two
git clone https://github.com/RAKWiskey/RAK831_LoRaGateway-test.git

-----------------------------------------------------------------------------------------

# [STEP 2] Install libftdi

sudo apt-get install libftdi-dev

# this should install :
# - libftdi-dev 0.19-4 (armhf)
# - libftdil 0.19-4 (armhf)
# - libusb-dev 2:0.1.12-20 (armhf)

-----------------------------------------------------------------------------------------

# [STEP 3] Go to the /libmpsse/src directory and install the library

sudo ./configure --disable-python

make

sudo make install
# Static and dynamic libraries compiled code is put into /usr/local/lib
# Header file is put into /usr/local/include

# On the Pcduino, you must regenerate the library cache (might some time).
sudo ldconfig

------------------------------------------------------------------------------------------

# [STEP 4] Unpack the LoRa Gateway project and go to lora_gateway directory. 
# then build the library and examples.
make all

------------------------------------------------------------------------------------------

# [STEP 5] Connect a nanoconcentrator and run test_loragw_reg to test that
# you have access to LoRa registers.go to lora_gateway/libloragw directory.
# Run the test LoRa gateway to receive the case.
sudo ./test_loragw_rx 868.1

------------------------------------------------------------------------------------------
