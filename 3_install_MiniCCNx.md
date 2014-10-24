# 3 - Install MiniCCNx

First of all, you need to know that your VM already has a CCN version that was automaticaly installed in NS-3 DCE installation, but this CCN installation isn't built do be used in MiniCCNx experiments.

In this section, you will install MiniCCNx to emulate yours CCNx experiments.

P.s: The entire procedure presented here was taken from the [MiniCCNx](https://github.com/chesteve/mn-ccnx/wiki) page.

## 3.1 - VM Route

First, configure routing in your VM:

`echo 1 > /proc/sys/net/ipv4/ip_forward`

## 3.2 - Prerequesites and Dependencies

Install some required dependencies.

```
apt-get -u install ant

apt-get install autoconf libssl-dev libexpat1-dev libpcap-dev libecryptfs0 libxml2-utils automake gawk gcc g++ git-core pkg-config libpcre3-dev mininet dia default-jre default-jdk git
```
Create and configure a account to be used by CCNx.

```
useradd -m ccnd
passwd -l ccnd             
rm -f /home/ccnd/.bash*
mkdir /var/log/ccnd
chown ccnd /var/log/ccnd
```

## 3.3 - Install CCNx

P.s: NS-3 DCE framework uses CCNx 0.6.2 version, so, you need to install same CCNx version in MiniCCNx. If you prefer, you can try to upgrade CCNx in Ns-3 DCE and MiniCCNx to use newer versions.










Now, you are able to continue installing others softwares needed. Continue [here](https://github.com/emersonbarea/testes/edit/master/3_install_MiniCCNx.md)
