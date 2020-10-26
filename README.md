# Tools

#### Install Environment Prereqs
###### GoLang
   * `sudo apt install golang -y`
   * Add /home/{USER}/go/bin to the PATH environment variable. You can do this by adding this line to your /etc/profile (for a system-wide installation) or $HOME/.profile:
       * `export PATH=$PATH:/home/{USER}/go/bin`
#### Install Go Tools/Add Binaries to PATH
   * `go get -u github.com/ropnop/kerbrute`
   * `go get -u github.com/sensepost/gowitness`
   * Run `source ~/.profile` to load binaries into path
#### Good Pentesting Tools/Wordlists Not Included with Kali
```
cd /opt/
sudo git clone https://github.com/joaomatosf/jexboss && cd jexboss && pip3 install -r requires.txt
cd /opt/
sudo git clone https://github.com/insidetrust/statistically-likely-usernames
sudo git clone https://github.com/danielmiessler/SecLists
sudo git clone https://github.com/FortyNorthSecurity/EyeWitness && cd EyeWitness/Python/setup/ && sudo ./setup.sh
cd /opt/
sudo git clone https://github.com/AonCyberLabs/Windows-Exploit-Suggester
sudo git clone https://github.com/SecWiki/windows-kernel-exploits
sudo git clone https://github.com/gentilkiwi/mimikatz
sudo pip3 install bloodhound
sudo apt install gobuster
sudo apt install bettercap -y
sudo apt install libreoffice -y

https://github.com/quentinhardy/odat/releases/
```
Additional tools may be installed by the tester before zbox deployment.

## Install Windows VM
#### VMware Player Setup
* Install Linux headers `sudo apt install linux-headers-$(uname -r) -y`
* https://www.vmware.com/go/getplayer-linux
* `sudo chmod +x [VMWARE_INSTALLER].bundle`
* `sudo ./[VMWARE_INSTALLER].bundle`
* If issues with GCC/vmmon/vmnet pop up, perform the following:
   * `sudo git clone -b workstation-$( grep player.product.version /etc/vmware/config | sed '/.*\"\(.*\)\".*/ s//\1/g' ) https://github.com/mkubecek/vmware-host-modules.git /opt/vmware-host-modules/`
   * `cd $_`
   * `sudo make`
   * `sudo make install`
