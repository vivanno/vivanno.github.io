---
title: Install Mullvad browser on Ubuntu
layout: "post"
date: 2024-03-17T18:55:10.311Z
preview: ""
tags: [ubuntu, mullvad, browser, privacy, firefox, mozilla]
categories: [quick-start]
type: default
---

# What is mullvad browser?
[Mullvad Browser](https://mullvad.net/en/download/browser/linux) is a privacy-focused web browser that is designed to enhance your online security and anonymity. It is based on the open-source [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/enterprise/). It is available for various operating systems, including [Ubuntu](https://ubuntu.com/download).


# Download the Mullvad signing key

```bash
$ sudo curl -fsSLo /usr/share/keyrings/mullvad-keyring.asc https://repository.mullvad.net/deb/mullvad-keyring.asc
```

# Add the Mullvad repository server to apt
    
```bash
$ echo "deb [signed-by=/usr/share/keyrings/mullvad-keyring.asc arch=$( dpkg --print-architecture )] https://repository.mullvad.net/deb/stable $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/mullvad.list
```

# Install the package

```bash
$ sudo apt update
$ udo apt install mullvad-browser
```