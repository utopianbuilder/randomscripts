# !/bin/bash
#
# Update APT & Install minimums
sudo apt update && sudo apt upgrade
sudo apt install hwlock htop  

#
# Download MoneroWallet
wget https://downloads.getmonero.org/cli/linux64/monero-linux-x6-v0.17.3.0.tar.bz2
tar -xf monero-linux-x6-v0.17.3.0.tar.bz2
#
# Download Monero Blockchain
wget https://downloads.getmonero.org/blockchain.raw
./monero-blockchain-import --verify 0 --input-file ./blockchain.raw
rm -rf ./blockchain.raw
#
# Download MoneroOcean Miner
cd
mkdir xmrig
cd xmrig
wget https://github.com/MoneroOcean/xmrig/releases/download/v6.8.1-mo2/xmrig-v6.16.4-mo1-lin64.tar.gz
tar xf xmrig-v6.16.4-mo1-lin64.tar.gz
sudo ./xmrig --benchmark=1M --submit
# Run Monero Deamon
./monerod
