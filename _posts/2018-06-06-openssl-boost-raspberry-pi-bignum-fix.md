---
layout: post
title: Boost + SSL compatability issue on Raspberry Pi
---

Today I came across a [simple fix for an issue that I come across when compiling many crypto wallets on the raspberry pi](https://github.com/BitzenyCoreDevelopers/bitzeny/issues/7).

The issue is that the latest openssl package is not compatable with the latest boost package.  This results in a big ugly error. 

Fortunately, HelloKS pointed out that this can be solved without compiling your own openssl.  Just install the previous version

```
sudo apt-get install libssl1.0-dev libssl1.0.2
```

Thank you [HelloKS](https://github.com/HelloKS)!

![_config.yml]({{ site.baseurl }}/images/crypto-wallet-ssl-fix.png)
