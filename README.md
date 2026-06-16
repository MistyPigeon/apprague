# Apprague

Apprague is a terminal-ran **Linux App Store** written in Python

# Adding your app

To add your app(s) **send a pull request with your apps repository link and we will compile and review it ourself.**

# Existing Linux app store formats supported

**Snap** and **Flatpak** is supported, **if your app is on either of those** we will get the Snap or Flatpak file (**tell us which one**) and we will add it to the repo

# App formats supported

**All Linux distro app formats is supported.**

# Config files

To make your app installable you need a manifest.yml, here is an example:
```
app_name: "Your App"
app_id: "your_app"
version: "1.2.0"
developer: "dev_name"
description: "An app of yours"
source: "https://github.com/user/your_app/releases/download/v1.2.0/binary-linux"

install:
  type: "binary" 
  destination: "$HOME/.local/bin/"
  dependencies:
    apt: ["libssl-dev"]
    pacman: ["openssl"]
    dnf: ["openssl-devel"]

```

