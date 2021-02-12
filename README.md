# Tools

### Install Environment Prereqs
#### Installing ZSH
   * Download oh-my-zsh
      * `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
   * Upgrade Prompt to PowerLevel10k
      * `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
   * Modify variables
      * `export ZSH="/root/.oh-my-zsh"`
      * `ZSH_THEME="powerlevel10k/powerlevel10k"`
   * Install Plugins
      1. Clone this repository into `$ZSH_CUSTOM/plugins` (by default `~/.oh-my-zsh/custom/plugins`)

         ```sh
         git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
         ```
      
      2. Clone this repository in oh-my-zsh's plugins directory:

         ```zsh
         git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
         ```

      3. Add the plugin to the list of plugins for Oh My Zsh to load (inside `~/.zshrc`):

         ```sh
         plugins=(zsh-autosuggestions, zsh-syntax-highlighting)
          ```


###### GoLang
   * `sudo apt install golang -y`
   * Add /home/{USER}/go/bin to the PATH environment variable. You can do this by adding this line to your /etc/profile (for a system-wide installation) or $HOME/.profile:
       * `export PATH=$PATH:~/go/bin`

#### Install Tools
   * `go get -u github.com/ropnop/kerbrute`
   * `go get -u github.com/sensepost/gowitness`
   * `apt-get install eyewitness`


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
