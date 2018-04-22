# Tellion-TLL A Coin Backed by A Business.

We aim to bring the forefront of PC & Cryptography Technology to the world alike


UNIX BUILD NOTES
====================

To Build Headless
-----------------

sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils

sudo apt-get install qt5-default qt5-qmake qtbase5-dev-tools qttools5-dev-tools build-essential libboost-dev libboost-system-dev libboost-filesystem-dev libboost-program-options-dev libboost-thread-dev libssl-dev libdb++-dev libminiupnpc-dev 

sudo apt-get install software-properties-common

sudo add-apt-repository ppa:bitcoin/bitcoin

sudo apt-get update

sudo apt-get install libdb4.8-dev libdb4.8++-dev

sudo apt-get install libqrencode-dev

git clone https://github.com/Tellion/Tellion.git

cd Tellion/src/secp256k1

chmod +x autogen.sh

sudo ./autogen.sh

sudo ./configure

sudo make && make install

cd

cd Tellion/src/leveldb

sudo sh build_detect_platform build_config.mk .

cd

cd Tellion/src

sudo make -f makefile.unix

strip telliond

LD_LIBRARY_PATH=/usr/local/lib

export LD_LIBRARY_PATH


To Build Qt Wallet
------------------

sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils

sudo apt-get install qt5-default qt5-qmake qtbase5-dev-tools qttools5-dev-tools build-essential libboost-dev libboost-system-dev libboost-filesystem-dev libboost-program-options-dev libboost-thread-dev libssl-dev libdb++-dev libminiupnpc-dev 

sudo apt-get install software-properties-common
sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install libdb4.8-dev libdb4.8++-dev

sudo apt-get install libqrencode-dev

git clone https://github.com/Tellion/Tellion.git

cd Tellion/src/secp256k1

chmod +x autogen.sh

sudo ./autogen.sh

sudo ./configure

sudo make && make install

cd

cd Tellion/src/leveldb

sudo sh build_detect_platform build_config.mk .

cd

cd Tellion

sudo qmake Tellion-TLL.pro

sudo make -jnumofcoreshere