# Compile Tutanota client on Ubuntu 14.14
The example shows how to compile the open sourced Tutanota
client so that you can host it yourself. Once you compile it,
you can host the client yourself, on your localhost for example. This has many benefits. First, the client loads faster as it only fetches files
from your localhost. Second, its safer. You host it yourself, so there is no reason to worry that suddenly the client code suddenly changes and adds some back-doors or something.  Third, you can modify it to your liking.  

The following instructions are based on those avaliable at [tutao/tutanota](https://github.com/tutao/tutanota/#building-and-running-your-own-tutanota-web-client).

```bash
# first we need to install package manager for nodejs called nmp
# this will also pull all its dependencies
sudo apt-get install npm

# get latest tutanota source code from github
git clone https://github.com/tutao/tutanota.git

cd tutanota/web

# download dependencies
npm install

# install gulp build system localy
npm install --save-dev gulp

# need to make the following sympolic link
# without it, gupl returns an error:
# /usr/bin/env: node: No such file or directory
sudo ln -s /usr/bin/nodejs /usr/local/bin/node

# build the tutanota client
../node_modules/gulp/bin/gulp.js dist

# check if the works example
firefox build/index.html

#Now you can copy the build folder to whereever you want it to be.
#For example, I have it /opt
sudo mv build/ /top/tuta

# now you can run the tutanota client as follows
firefox /opt/tuta/index.html
```

## What it has to do with Monero?
Well, both [Tutanota](https://tutanota.com/) and [Monero](https://getmonero.org) take privacy of their users seriously.

## How can you help?

Constructive criticism, corrections of the website are always welcome.  
They can be made through gihub.

Some Monero are also welcome:
```
48daf1rG3hE1Txapcsxh6WXNe9MLNKtu7W7tKTivtSoVLHErYzvdcpea2nSTgGkz66RFP4GKVAsTV14v6G3oddBTHfxP6tU
```
