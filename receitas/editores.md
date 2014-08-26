## Install Atom Editor
- https://github.com/atom/atom/tree/master/docs/build-instructions/linux.md

```
sudo apt-get install libgnome-keyring-dev
npm config set python /usr/bin/python2 -g
git clone https://github.com/atom/atom
cd atom
script/build # Creates application at $TMPDIR/atom-build/Atom
sudo ln -s /home/fabricio/.nvm/v0.10.30/bin/node /usr/bin/node
sudo script/grunt install # Installs command to /usr/local/bin/atom
script/grunt mkdeb
```

### Update Atom

antes = 0.108.0-092dac7

```
git pull
npm config set python /usr/bin/python2 -g
script/build
sudo script/grunt install
script/grunt mkdeb
```
depois = 0.122.0-16fd14d
