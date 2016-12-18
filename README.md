This is official repository for the StomLib library, an open-source project that can work with Blizzard MPQ archives.

### This fork
..is used to contribute patches upstream and to provide information on Linux packaging.

### Debian 7 (amd64)
 1. To `/etc/apt/sources.list` add:

    ```
    #apt.xpam.pl
    deb https://apt.xpam.pl/ jessie main
    ```

 2. Add GPG key: `wget -qO - https://apt.xpam.pl/xpam.pl-pubkey.asc | sudo apt-key add -`
 3. Update and install: `sudo apt-get update && sudo apt-get install stormlib`

### Recent Fedora releases
 ```
dnf config-manager --add-repo https://rpm.xpam.pl
rpm --import https://rpm.xpam.pl/rpm-pubkey.asc
dnf install bncsutil
```

### Centos 7
```
yum install yum-utils
yum-config-manager --add-repo https://centos7.rpm.xpam.pl
yum-config-manager --enable https://centos7.rpm.xpam.pl
rpm --import https://centos7.rpm.xpam.pl/rpm-pubkey.asc
yum install stormlib
```
### Centos 6
```
yum install yum-utils
yum-config-manager --add-repo https://centos6.rpm.xpam.pl
yum-config-manager --enable https://centos6.rpm.xpam.pl
rpm --import https://centos6.rpm.xpam.pl/rpm-pubkey.asc
yum install stormlib
```
