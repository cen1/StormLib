This is official repository for the StomLib library, an open-source project that can work with Blizzard MPQ archives.

### This fork
..is used to contribute patches upstream and to provide information on Linux packaging.

### Build tips

#### DEB
```
apt-get update
apt-get -y install apt-transport-https
apt-get -y install build-essential cmake git
apt-get -y install zlib1g-dev libbz2-dev
git clone https://github.com/cen1/StormLib.git
cd StormLib
git checkout v9.22
cmake -G "Unix Makefiles" -H./ -B./build -DBUILD_SHARED_LIBS=true
cd build
make
cpack -G "DEB"
```

#### RPM
```
yum -y update
yum -y groupinstall "Development Tools"
yum -y install cmake git zlib-devel bzip2-devel nano
git clone https://github.com/cen1/StormLib.git
cd StormLib
git checkout v9.22
cmake -G "Unix Makefiles" -H./ -B./build -DBUILD_SHARED_LIBS=true
cd build
make
cpack -G "RPM"
```

### Debian 8 and 9 (amd64)
 1. To `/etc/apt/sources.list` add:

#### 9
```
#apt.xpam.pl
deb http://apt.xpam.pl/debian9/ bnetdocs-stretch main
```
#### 8
```
#apt.xpam.pl
deb http://apt.xpam.pl/debian8/ bnetdocs-jessie main
```

 2. Add GPG key: `wget -qO - https://apt.xpam.pl/xpam.pl-pubkey.asc | sudo apt-key add -`
 3. Update and install: `sudo apt-get update && sudo apt-get install stormlib`


### Centos 7
```
yum -y install yum-utils
yum-config-manager --add-repo https://centos7.rpm.xpam.pl
yum-config-manager --enable https://centos7.rpm.xpam.pl
rpm --import https://centos7.rpm.xpam.pl/xpam.pl-pubkey.asc
yum -y install stormlib
```
### Centos 6
```
yum -y install yum-utils
yum-config-manager --add-repo https://centos6.rpm.xpam.pl
yum-config-manager --enable https://centos6.rpm.xpam.pl
rpm --import https://centos6.rpm.xpam.pl/xpam.pl-pubkey.asc
yum -y install stormlib
```
