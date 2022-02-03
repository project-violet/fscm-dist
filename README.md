# fscm-dist

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
