# Tutorial for customizing a terminal

## Start with installing the `zsh` in your system
```sh
 sudo apt install zsh
 ```
 **Output**

 ```sh
 Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  zsh-common
Suggested packages:
  zsh-doc
The following NEW packages will be installed:
  zsh zsh-common
0 upgraded, 2 newly installed, 0 to remove and 0 not upgraded.
Need to get 4794 kB of archives.
After this operation, 18.2 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu jammy/main amd64 zsh-common all 5.8.1-1 [3985 kB]
Get:2 http://archive.ubuntu.com/ubuntu jammy/main amd64 zsh amd64 5.8.1-1 [809 kB]
Fetched 4794 kB in 13s (366 kB/s)
Selecting previously unselected package zsh-common.
(Reading database ... 44588 files and directories currently installed.)
Preparing to unpack .../zsh-common_5.8.1-1_all.deb ...
Unpacking zsh-common (5.8.1-1) ...
Selecting previously unselected package zsh.
Preparing to unpack .../archives/zsh_5.8.1-1_amd64.deb ...
Unpacking zsh (5.8.1-1) ...
Setting up zsh-common (5.8.1-1) ...
Setting up zsh (5.8.1-1) ...
Processing triggers for man-db (2.10.2-1) ...
```
## paste the following command into your terminal. You can also get the link from the [ohmy-zsh](https://ohmyz.sh/) website.
```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
**Output**
```sh
Cloning Oh My Zsh...
remote: Enumerating objects: 1428, done.
remote: Counting objects: 100% (1428/1428), done.
remote: Compressing objects: 100% (1364/1364), done.
remote: Total 1428 (delta 39), reused 1135 (delta 36), pack-reused 0 (from 0)
Receiving objects: 100% (1428/1428), 3.26 MiB | 223.00 KiB/s, done.
Resolving deltas: 100% (39/39), done.
From https://github.com/ohmyzsh/ohmyzsh
 * [new branch]      master     -> origin/master
Branch 'master' set up to track remote branch 'master' from 'origin'.
Already on 'master'
/home/usr

Looking for an existing zsh config...
Using the Oh My Zsh template file and adding it to /home/genomics/.zshrc.

Time to change your default shell to zsh:
Do you want to change your default shell to zsh? [Y/n] y
Changing your shell to /usr/bin/zsh...
[sudo] password for `user_account`:
Shell successfully changed to '/usr/bin/zsh'.


         __                                     __
  ____  / /_     ____ ___  __  __   ____  _____/ /_
 / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \
/ /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / /
\____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/
                        /____/                       ....is now installed!


Before you scream Oh My Zsh! look over the `.zshrc` file to select plugins, themes, and options.

• Follow us on X: https://x.com/ohmyzsh
• Join our Discord community: https://discord.gg/ohmyzsh
• Get stickers, t-shirts, coffee mugs and more: https://shop.planetargon.com/collections/oh-my-zsh
```
### Upto this point you have succesfully changed your terminal/ shell. It will have the following look.

```sh
➜  ~  
```
### You may wish to do more cutomization.
### **Autosuggestions**

Run the following code into your terminal
```sh
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```
**Output**
```sh
Cloning into '/home/genomics/.oh-my-zsh/custom/plugins/zsh-autosuggestions'...
remote: Enumerating objects: 2577, done.
remote: Counting objects: 100% (192/192), done.
remote: Compressing objects: 100% (102/102), done.
remote: Total 2577 (delta 117), reused 139 (delta 86), pack-reused 2385 (from 1)
Receiving objects: 100% (2577/2577), 590.57 KiB | 1019.00 KiB/s, done.
Resolving deltas: 100% (1648/1648), done.
```
Set the `zsh` autosuggestion into the `zsh configuration` folder. Use any text editor such as `vs code` `gedit` `nano` or `vim` to open the `.zshrc` file. In this case I used vs code.
```sh
code ~/.zshrc
```
edit the plugins which will first be looking like this

```
plugins=(git)
```
add `zsh-autosuggestions` in the brackets and save the file.
```
plugins=(git zsh-autosuggestions)
```
To activate the changes and make it work, write the following code
```sh
source ~/.zshrc
```
Done. The autosuggestion is now working :smile:

### **Installing themes**
watch more in this [youtube video](https://www.youtube.com/watch?v=WVQuv664qsk) from minute `7:13` for further guidance.
