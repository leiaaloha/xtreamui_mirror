# Xtream UI for Ubuntu 22.04 install
This is an installation mirror for xtream ui software on Ubuntu 22.04.
Includes NGINX 1.19.2 and PHP 7.3.25.

Required to run
sudo apt update

sudo apt upgrade -y

sudo apt install  -y python-is-python3

wget http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1-1ubuntu2.1~18.04.23_amd64.deb

sudo dpkg -i libssl1.1_1.1.1-1ubuntu2.1~18.04.23_amd64.deb

wget http://mirrors.kernel.org/ubuntu/pool/universe/libz/libzip/libzip5_1.5.1-0ubuntu1_amd64.deb

echo "APT::Sandbox::User \"root\";" > /etc/apt/apt.conf.d/10sandbox

sudo apt install ./libzip5_1.5.1-0ubuntu1_amd64.deb

sudo reboot (YES REBOOT)

wget https://github.com/leiaaloha/xtreamui_mirror/raw/master/install3.py;

sudo python3 install3.py;

### 12/27/2023 ###
VOD/Series bug in python, need to update release.py with print() or change to php

### Update 08/03/2021: ###
- No planned update to come


### Update 11/01/2021: ###
- Fixed release
- Bumped xtream-ui admin to 22F Mods 13


### Update 08/12/2020: ###
- bumped php version from 7.2 to 7.3 following 7.2 obsolence
- fixed user_watcher.php disconnect users every minute because of wrong pid check.

Note: HLS activity is wrongly reported. You should use mpegts ouput and not hls while it's unfixed

### THANKS ###

Thanks to GTA for xtream-ui admin original interface
Thanks to emre1393 for being the wisdom of xui community

### Installation: ###

Update your ubuntu first, then install panel:
``` 
sudo apt update && sudo apt full-upgrade -y && sudo apt install python2 -y;  
wget https://github.com/leiaaloha/xtreamui_mirror/raw/master/install3.py; 
sudo python3 install3.py 
```
  
If you want a whole NEW installation, choose MAIN and then UPDATE.  
If you want to install load balance on additional servers, add a server to panel in manage servers page, then run script and proceed with LB option.  
If you want to update admin panel, select UPDATE.

### Video tutorials : ###

[Xtream-UI Tutorials](https://www.youtube.com/playlist?list=PLJB51brdC_w7dTDxi1MPqiuk3JH5U2ekn "Xtream-UI Tutorials")

