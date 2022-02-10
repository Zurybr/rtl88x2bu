# How to Install TP-Link Archer T4U Driver 
## Installing the Driver
### 1. First open terminal and install dkms

    sudo apt-get update
    sudo apt-get install dkms
### 2. Copy the following commands

    git clone https://github.com/Zurybr/rtl88x2bu.git
    cd rtl88x2bu
    VER=$(sed -n 's/\PACKAGE_VERSION="\(.*\)"/\1/p' dkms.conf)
    sudo rsync -rvhP ./ /usr/src/rtl88x2bu-${VER}
    sudo dkms add -m rtl88x2bu -v ${VER}
    sudo dkms build -m rtl88x2bu -v ${VER}
    sudo dkms install -m rtl88x2bu -v ${VER}
    sudo modprobe 88x2bu

### 3. Plug your tp-link
<br />
<br />

## Build confirmed on: 


```
Linux version 5.4.0-4-amd64 (debian-kernel@lists.debian.org) (gcc version 9.2.1 20200203 (Debian 9.2.1-28)) #1 SMP Debian 5.4.19-1 (2020-02-13)
```

## Original repo 


If you want to read more please visit 
[rtl88x2bu](https://github.com/cilynx/rtl88x2bu),
the original repo was made by cilynx.
