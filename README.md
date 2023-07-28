# LinuxGuide
## 1. Give Sudo Privileges to a User
### 1.1. Switch to Root User
  - run `su` in terminal to switch to Root user
### 1.2. Edit the Sudoers File
  - run `nano /etc/sudoers` to open the sudo config file
    - *you can use any file editor like `vim` instead of `nano` 
  - add  `USER ALL=(ALL) ALL` to the file and replace `USER` with your username
    - for `nano`:
      - `shift + ctrl + v` to paste 
      -  `ctrl + o` to save changes
      -  `ctrl + x`to exit
## 2. Update & Upgrade the System
- run `sudo apt update`
- after that run `sudo apt upgrade -y`
- run `reboot` to restart your pc
  
