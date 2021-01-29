# Tools



### Install Environment Prereqs
#### Installing ZSH


###### GoLang
   * `sudo apt install golang -y`
   * Add /home/{USER}/go/bin to the PATH environment variable. You can do this by adding this line to your /etc/profile (for a system-wide installation) or $HOME/.profile:
       * `export PATH=$PATH:/home/{USER}/go/bin`
#### Install Go Tools/Add Binaries to PATH
   * `go get -u github.com/ropnop/kerbrute`
   * `go get -u github.com/sensepost/gowitness`
   * Run `source ~/.profile` to load binaries into path

## Install Windows VM (if needed)
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
