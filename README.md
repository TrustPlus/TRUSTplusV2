
## TRUSTplusV2

Official inital implementation of the TRUSTplus core.

[![Discord](https://img.shields.io/badge/Chat-on%20Discord-blue.svg)](https://discord.gg/56Dfku) 
[![Slack](https://img.shields.io/badge/Chat-on%20Slack-red.svg)](https://join.slack.com/t/trustplus/shared_invite/enQtNTE3MjU1MTM2MzA4LTMwNWRjMDAxMDI1NWMwZDY0YWNjYWRhNDNjNzA3Y2VlNDkxOGM2MDkzNjc5Zjk5ZGQxZTQ0MWNiN2RiYzRhY2M) 
[![IRCchat](https://img.shields.io/badge/Chat-on%20IRCchat-brightgreen.svg)](http://webchat.freenode.net/?channels=trustpluscoin)

## Chapter 2 of TrustPlus
TRUSTplusV2 is a continuation of the TRUST project that was based upon a pure PoS Blockchain on the X11 algorithm.  This project stood the test of time, launching 7/4/14. Today we start TRUSTplusV2 (Trust-Plus-Version-2) on 2019 New Years as a PoW Blockchain on X16S algorithm with Masternodes.

## Rewards
TrustPlusV2 is strait forward: 10 TRUST per block, 50% is created for the winning masternode, halving in increments of 500,000 blocks. The first period extended to 700,000 blocks.

There is a 35,000,000 TRUST block reward at block 1 to fund the TRUSTv1 to TRUSTv2 swap.
The first 9600 blocks rewards are 0.1 with 1% of the reward going to Masternodes.

Source: https://github.com/TrustPlus/TRUSTplusV2/tree/src/main.cpp#L1746

## Building the source

`sudo add-apt-repository ppa:bitcoin/bitcoin`

`sudo apt-get update`

`sudo apt-get install git zip unzip -y`

```
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev libboost-all-dev software-properties-common libdb*-dev libdb*++-dev libminiupnpc-dev libzmq3-dev software-properties-common -y
```

If you are making a headless server, please skip this next step.

```
sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler libqrencode-dev libzmq3-dev
```

`git clone git://github.com/TrustPlus/TRUSTplusV2`

`cd TRUSTplusV2`

`./autogen.sh`

`./configure`

`make`

**Note some Servers will require sudo**

## Executables

Source should be inside ~/TRUSTplusV2/src folder
QT files are inside ~/TRUSTplusV2/src/qt folder

## Running trustplusd

It is recommended to run trustplusd or trustplus-qt in terminal with the flag -printtoconsole for Ubuntu. 

## Running TrustPlus-QT

It is also recommended to use CMD for windows to run trustplusd.exe or trustplus-qt.exe with the -printtoconsole flag. 

### Configuration

The configuration file is inside the Unix folder ~/.trustpluscore or Windows %appdata%/TRUSTplusCore as trustplus.conf

```
rpcuser=rpcUser
rpcpassword=<changeMe>
rpcport=37001
rpcallowedip=127.0.0.1
addnode=seed1.trustplus.com
addnode=seed2.trustplus.com
addnode=seed3.trustplus.com
addnode=seed4.trustplus.com
addnode=seed5.trustplus.com
addnode=seed6.trustplus.com
addnode=miner1.trustplus.com
addnode=miner2.trustplus.com
addnode=mn1.trustplus.com
```

#### Mining

Create an TRUST Wallet. Setup your trustplus.conf file. Use cpuminer-opt from https://github.com/JayDDee/cpuminer-opt 

Example commandline for cpuminer is:

./cpuminer -a x16s -o http://127.0.0.1:37001/ -u rpcUserXX -p rpcPasswprdXX --coinbase-add=TmmDpEvmgrxxxxxxxxxxxxxxxxxxxxxxx --no-getwork --debug

Coinbase address is the wallet address you would like the reward to goto. Debug is always helpful.

#### Building a masternode

We created a Wiki page here. https://github.com/TrustPlus/TRUSTplusV2/wiki/Making-an-TRUST-MasterNode-Step-by-Step Please suggest adds and comment.

## Contribution
!! working Document !! Original Layout belongs to EthereumGo https://github.com/ethereum/go-ethereum

## License

The software is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or the use or other dealings in the software.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.


Copyright (c) 2018 TRUSTplusV2
