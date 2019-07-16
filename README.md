### gitian-builder
---
https://github.com/devrandom/gitian-builder

```
```

```sh
sudo pacman -S python2-cheetah qemu rsync
sudo pacman -S lxc libvirt bridge-utils

layman - a luke-jr
sudo emerge dev-vcs/git net-misc/apt-cacher-ng app-emulation/vmbuilder dev-lang/ruby
sudo emerge app-emulation/qemu
export KVM=qemu-system-x86_64

sudo apt-get install git apache2 apt-cacher-ng python-vm-builder ruby qemu-utils
sudo apt-get install lxc
sudo apt-get install docker-ce

sudo apt-get install ubuntu-archive-keyring
sudo port install ruby coreutils
export PATH=$PATH:/opt/locallibexec/gnunbin

brew install ruby coreutils
export PATH=$PATH:/opt/local/libexec/gnubin

bin/make-base-vm --distro debian --suite jessie

bin/make-base-vm
bin/make-base-vm --arch i386

bin/make-base-vm --lxc
bin/make-base-vm --lxc --arch i386

export USE_LXC=1

bin/make-base-vm --docker
bin/make-base-vm --docker --arch i386

export USE_DOCKER=1

VBoxManage modifyvm Gitian-xenial-i386 --natpf1 "guestssh,,2233,,22"

ssh-keygen -t rsa -f var/id_rsa -N ""
ssh -p 2223 ubuntu@localhost 'mkdir -p .ssh && chmod 700 .ssh && cat >> .ssh/authorized_keys' < var/id_rsa.pub

ssh -p 2223 ubuntu@localhost
sudo bash
mkdir -p .ssh && chomd 700 .ssh && cat ~ubuntu/.ssh/authorized_keys >> .ssh/authorized_keys

export USE_VBOX=1

PATH=$PATH:$(pwd)/libexec
make-claen-vm --suite xenial --arch i386

DISTRO=debian

LXC_ARCH=i386 LXC_SUITE=xenial on-target ls -la

start-target 32 xenial-i386 &
on-target ls -la
stop-target

export USE_LXC=1
bin/gbuild <package>.yml

bin/gbuild --commit <dir>=<hash> <package>.yml

bin/gsign --signer <signer> --release <release-name> <package>.yml
bin/gverify --release <release-name> <package>.yml

%admin ALL=NOPASSWD: /usr/bin/lxc-execute
%admin ALL-NOPASSWD: /usr/bin/lxc-start

export LXC_EXECUTE=lxc-execute
sudo brctl addbr br0
sudo ifconfig br0 10.0.2.2/24 up

python -m unittest discover test
```

```
```


