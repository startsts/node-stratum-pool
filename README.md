High performance Stratum poolserver in Node.js. One instance of this software can startup and manage multiple coin
pools, each with their own daemon and stratum ports :)

This software has been modefied for merged mining. It is still in development.

#### Notice
This is a module for Node.js that will do nothing on its own. Unless you're a Node.js developer who would like to
handle stratum authentication and raw share data then this module will not be of use to you.

[![Build Status](https://travis-ci.org/KillerByte/node-stratum-pool.png?branch=master)](https://travis-ci.org/KillerByte/node-stratum-pool)

#### Why
This server was built to be more efficient and easier to setup, maintain and scale than existing stratum poolservers
which are written in python. Compared to the spaghetti state of the latest
[stratum-mining python server](https://github.com/Crypto-Expert/stratum-mining/), this software should also have a
lower barrier to entry for other developers to fork and add features or fix bugs.


Features
----------------------------------
* Merged Mining Support
* Daemon RPC interface
* Stratum TCP socket server
* Block template / job manager
* P2P to get block notifications as peer node
* Optimized generation transaction building
* Connecting to multiple daemons for redundancy
* Process share submissions
* Session managing for purging DDoS/flood initiated zombie workers
* Auto ban IPs that are flooding with invalid shares
* __POW__ (proof-of-work) & __POS__ (proof-of-stake) support
* Transaction messages support
* Vardiff (variable difficulty / share limiter)
* When started with a coin daemon that hasn't finished syncing to the network it shows the blockchain download progress and initializes once synced

#### Hashing algorithms supported:
* ✓ __SHA256__ (Bitcoin, Freicoin, Peercoin/PPCoin, Terracoin, etc..)
* ✓ __Scrypt__ (Litecoin, Dogecoin, Feathercoin, etc..)
* ✓ __Scrypt-Jane__ (YaCoin, CopperBars, Pennies, Tickets, etc..)
* ✓ __Scrypt-N__ (Vertcoin [VTC])
* ✓ __Quark__ (Quarkcoin [QRK])
* ✓ __X11__ (Darkcoin [DRK], Hirocoin, Limecoin)
* ✓ __X13__ (MaruCoin, BoostCoin)
* ✓ __NIST5__ (Talkcoin)
* ✓ __Keccak__ (Maxcoin [MAX], HelixCoin, CryptoMeth, Galleon, 365coin, Slothcoin, BitcointalkCoin)
* ✓ __Skein__ (Skeincoin [SKC])
* ✓ __Groestl__ (Groestlcoin [GRS])

May be working (needs additional testing):
* ? *Blake* (Blakecoin [BLC])
* ? *Fugue* (Fuguecoin [FC])
* ? *Qubit* (Qubitcoin [Q2C], Myriadcoin [MYR])
* ? *SHAvite-3* (INKcoin [INK])

Not working currently:
* *Groestl* - for Myriadcoin
* *Keccak* - for eCoin & Copperlark
* *Hefty1* (Heavycoin [HVC])


Requirements
------------
* node v0.10+
* coin daemon for primay and auxillery coins (preferably one with a relatively updated API and not some crapcoin :p)


Example Usage
-------------

#### Install as a node module by cloning repository

```bash
git clone https://github.com/KillerByte/node-stratum-pool node_modules/stratum-pool
npm update
```

#### Module usage

Please see the included example.js file for more information. This section should be
expanded soon.

Credits
-------
* [zone117x](//github.com/zone117x) - Head developer of the original stratum mining pool for node.js
* [vekexasia](//github.com/vekexasia) - co-developer & great tester
* [LucasJones](//github.com/LucasJones) - got p2p block notify working and implemented additional hashing algos
* [TheSeven](//github.com/TheSeven) - answering an absurd amount of my questions, found the block 1-16 problem, provided example code for peer node functionality
* [pronooob](https://dogehouse.org) - knowledgeable & helpful
* [Slush0](//github.com/slush0/stratum-mining) - stratum protocol, documentation and original python code
* [viperaus](//github.com/viperaus/stratum-mining) - scrypt adaptions to python code
* [ahmedbodi](//github.com/ahmedbodi/stratum-mining) - more algo adaptions to python code
* [steveshit](//github.com/steveshit) - ported X11 hashing algo from python to node module


Donations
---------
To support development of this project to the original author (zone117x), feel free to donate :)

* BTC: `1KRotMnQpxu3sePQnsVLRy3EraRFYfJQFR`
* LTC: `LKfavSDJmwiFdcgaP1bbu46hhyiWw5oFhE`
* VTC: `VgW4uFTZcimMSvcnE4cwS3bjJ6P8bcTykN`
* MAX: `mWexUXRCX5PWBmfh34p11wzS5WX2VWvTRT`
* QRK: `QehPDAhzVQWPwDPQvmn7iT3PoFUGT7o8bC`
* DRK: `XcQmhp8ANR7okWAuArcNFZ2bHSB81jpapQ`
* DOGE: `DBGGVtwAAit1NPZpRm5Nz9VUFErcvVvHYW`
* Cryptsy Trade Key: `254ca13444be14937b36c44ba29160bd8f02ff76`

License
-------
Released under the GNU General Public License v2

http://www.gnu.org/licenses/gpl-2.0.html
