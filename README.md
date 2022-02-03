# fscm-dist

base: https://github.com/project-violet/violet-message-search/blob/master/MANUAL.md

## merge

```sh
sudo apt update -y
sudo apt install unzip nginx libgomp1 -y

sudo su
mkdir htext-miner
cd htext-miner
wget https://github.com/project-violet/fscm-dist/releases/download/21.12.26/hentai-cache-backup-2021.12.26.zip -o cache.zip
unzip cache.zip
wget https://github.com/project-violet/fscm-dist/raw/main/hcache-merger
chmod 777 hcache-merger
./hcache-merger 3
```

## fscm

```sh
sudo apt update -y
sudo apt install libgomp1 -y
sudo su
mkdir -p /var/swap
dd if=/dev/zero of=/var/swap/swapfile bs=1M count=4000
mkswap -f /var/swap/swapfile
swapon /var/swap/swapfile
swapon -s

wget https://github.com/project-violet/fscm-dist/raw/main/fscm
wget https://raw.githubusercontent.com/project-violet/fscm-dist/main/forever.py
```
