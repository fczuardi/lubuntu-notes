## Install Atom Editor
- https://github.com/atom/atom/tree/master/docs/build-instructions/linux.md

```
sudo apt-get install libgnome-keyring-dev
npm config set python /usr/bin/python2 -g
git clone https://github.com/atom/atom
cd atom
script/build # Creates application at $TMPDIR/atom-build/Atom
sudo ln -s /home/fabricio/.nvm/v0.10.28/bin/node /usr/bin/node
sudo script/grunt install # Installs command to /usr/local/bin/atom
script/grunt mkdeb
```
