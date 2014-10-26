# 4 - FNSS

[FNSS](http://fnss.github.io/) is a toolchain to setup a network experiment scenario.

We will use `FNSS` to generate topology and traffic matrix in our emulated experiments (`MiniCCNx`) and simulated experiments (`NS-3 DCE`).

## 4.1 - Install FNSS to emulate

You only need to install `FNSS core`. Do it following the step bellow:

`curl -L https://github.com/fnss/fnss/raw/master/core/ubuntu_install.sh | sh`

This procedure install `FNSS core` files in `/usr/local/lib/python2.7/dist-packages/fnss` directory.

### 4.1.1 - FNSS core test

To test `FNSS core` installation, you can do the test bellow:

```
/opt/# python
Python 2.7.6 (default, Mar 22 2014, 22:59:56)
[GCC 4.8.2] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> import fnss
>>> topo = fnss.two_tier_topology(1,2,2)
>>> fnss.write_topology(topo, 'fnss-topo.xml')
>>>
root@ndnsimdbg:/opt/fnss/core/tocha# ls
fnss-topo.xml
root@ndnsimdbg:/opt/fnss/core/tocha# vi fnss-topo.xml
root@ndnsimdbg:/opt/fnss/core/tocha#
root@ndnsimdbg:/opt/fnss/core/tocha#
root@ndnsimdbg:/opt/fnss/core/tocha#
root@ndnsimdbg:/opt/fnss/core/tocha# mn-fnss fnss-topo.xml
*** Creating network
*** Adding controller
*** Adding hosts:
h1 h2 h3 h4
*** Adding switches:
s1 s2 s3
*** Adding links:
(h1, s2) (h2, s2) (h3, s3) (h4, s3) (s1, s2) (s1, s3)
``` 

### 4.1.2.- FNSS to simulated experiments

Now, you are able to continue installing others softwares needed. Continue [here](https://github.com/emersonbarea/testes/edit/master/4_install_FNSS.md).
