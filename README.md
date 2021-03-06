

Gitpay Coin integration/staging repository
======================================


***

Quick installation of the gitpay daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/gitpayproject/gitpay.git
    cd gitpay
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip GITSd
    sudo strip GITS-cli
    sudo strip GITS-tx
    cd ..

Running the daemon:

    GITSd 

Stopping the daemon:

    GITS-cli stop

Demon status:

    GITS-cli getinfo
    GITS-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/GitPayProject/gitpay/releases

P2P port: 33358, RPC port: 33359
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
