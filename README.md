TheCoin Aims to support cannabis seeds sales worldwide with private growers and some of the best strains available to date.

The goal of the project is offering a decentralized system that rewards you with the availability of trade to seeds on the website https://thethccoin.com/

Other Official Links here:

https://bitcointalk.org/index.php?topic=5255871.new#new BTCANN

https://github.com/mrwhalebones/thc GITHUB

https://thexplorer.thethccoin.com/ EXPLORER

https://twitter.com/TheCoin16 TWITTER



Name: TheCoin

Ticker: THC

Compiling OS: Ubuntu 18.04 LTS

Algorithm:   Scrypt

Block type: Proof-of-Work/Proof-of-Stake

Coin name: TheCoin

Coin abbreviation: THC

Address letter: T

Address letter testnet: C

RPC port: 20349

P2P port: 20350

Block reward (PoW): 50 coins

Block reward (PoS): 15 coins

Coin supply from PoW: 38000~ coins (less due to POS block rewards)

Coin supply from PoS: Indefinite

Last PoW block: block 759( live update (hardcoded 1000))

Min. stake age: 5 hours

Max. stake age:   Unlimited

Coinbase maturity: 24 blocks

Target spacing for PoW: 5 minutes

Target timespan: Average 25 minutes on a 30 day period

Transaction confirmations:   23 blocks

Node 1   
137.220.32.227
Node 2
155.138.233.183


Below are guidelines for setting up a linux node. I tried to make things as simple as possible to build, if you are knowledgeable in compiling, this will be a breeze.

Enter these commands to update, upgrade, and install required libraries and dependencies on your VPS

sudo apt-get update 

sudo apt-get upgrade 

sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3 libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev libboost-all-dev libboost-program-options-dev 

sudo apt-get install libminiupnpc-dev libzmq3-dev libprotobuf-dev protobuf-compiler unzip software-properties-common 

sudo add-apt-repository ppa:bitcoin/bitcoin 

sudo apt-get install libdb5.3++ 

sudo apt-get install libdb4.8-dev libdb4.8++-dev 

sudo apt-get update 

Use these next commands to download and install the binaries.

wget "https://github.com/mrwhalebones/thc/releases/download/V1.0/thecoin-daemon-linux.tar.gz" -O thecoin-daemon-linux.tar.gz 

wget "https://github.com/mrwhalebones/thc/releases/download/V1.0/thecoin-qt-linux.tar.gz" -O thecoin-qt-linux.tar.gz 

tar -xzvf thecoin-daemon-linux.tar.gz 

tar -xzvf thecoin-qt-linux.tar.gz 

sudo mv thecoind thecoin-cli thecoin-tx /usr/bin/ 

mkdir $HOME/.thecoin 

nano $HOME/.thecoin/thecoin.conf 


Copy and paste this into the .conf file you just created and remove any extra lines or spaces.

rpcuser=randomuser

rpcpassword=randompass

rpcallowip=127.0.0.1

rpcport=20349

listen=1

server=1

txindex=1

daemon=1


Now run the daemon with this command.

thecoind

Happy mining and staking!
