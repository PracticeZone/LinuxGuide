# My Personal Linux Guide
## Table of Content
- [1. Give Sudo Privileges to a User](#1-give-sudo-privileges-to-a-user)
- [2. Update & Upgrade the System](#2-update--upgrade-the-system)
- [3. add reboot & poweroff commands](#3-add-reboot--poweroff-commands)
- [5. Installing NodeJS](#5-installing-nodejs)
- [6. Installing Flutter](#6-installing-flutter)
- [7. Installing Android Studio](#7-installing-android-studio)

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
      -  `ctrl + x` to exit
## 2. Update & Upgrade the System
- run `sudo apt update`
- after that run `sudo apt upgrade -y`
- run `reboot` to restart your pc

## 3. add `reboot` & `poweroff` commands
- if you facing:
  - `bash: poweroff: command not found`
  - `bash: reboot: command not found`
- run `nano ~/.bashrc` in terminal to open `.bashrc` file
- add these two lines
  ``` bash
  alias reboot='systemctl reboot'
  alias poweroff='systemctl poweroff'
  ```

## 4. Installing Window Manager (Qtile)
   - installing dependencies
     ``` shell
       sudo apt install xserver-xorg xinit libpangocairo-1.0-0 python3-pip python3-xcffib python3-cairocffi
     ```
   - install Qtile
     ``` shell
       pip3 install qtile --break-system-packages
     ```

## 5. Installing NodeJS
visit: https://github.com/nodesource/distributions

## 6. Installing Flutter
 - download Flutter SDK: https://docs.flutter.dev/get-started/install/linux
 - extract `flutter_linux...tar.xz` in `home` directroy or anywhere you want
 - add this line `export PATH="$PATH:$HOME/flutter/bin"` in `.bashrc` to export the Flutter Path
    - *if you didn't extract Flutter SDK in `home` replace `$HOME` with your path
  
## 7. Installing Android Studio
  - download it from: https://developer.android.com/studio
  - extarct `android-studio...tar.xz` in `home` directroy or anywhere you want 
  - open terminal in `/android-studio/bin` and run `sh studio.sh`
