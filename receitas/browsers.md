
## Install Uzbl

```
sudo apt-get install uzbl
```

### Fazer yu e yU copiarem para common clipboard ao inves de primary
- editar ~/.config/uzbl/config la pela linha #325

```
@cbind  yu  = sh 'echo -n "$UZBL_URI" | xclip -selection common'
@cbind  yU  = sh 'echo -n "$1" | xclip -selection common' '\@SELECTED_URI'
```

### Como fazer buscas no Uzbl

- digite ```ddg <sua busca>```

## Substituir Firefox por Icecat

- http://ftp.gnu.org/gnu/gnuzilla/
  - ver a ultima versao
- http://www.debianadmin.com/how-to-install-icecat-and-icedove-on-debian-7-wheezy.html

```
sudo apt-get autoremove firefox
wget http://ftp.gnu.org/gnu/gnuzilla/24/icecat-24.0-64bit.tar.gz
tar -xvf icecat-24.0-64bit.tar.gz
mv icecat-24.0 ~/Applications/.
sudo ln -s /home/fabricio/Applications/icecat-24.0/icecat /usr/bin/browser
```

## Fazer o IceCat ser mais parecido com o Uzbl
- instalar https://addons.mozilla.org/en-US/firefox/addon/hide-tab-bar-with-one-tab/
- esconder todas as toolbars
- Ctrl+l = location bar
- Ctrl+k = search
- Ctrl+Shift+Y = downloads

## Instalar Chromium
- ```sudo apt-get install chromium-browser```
- "Use system title bar and borders"
- dar quit no applet de keyboard do lubuntu (ibus??)
  - http://www.ubuntuask.com/q/answers-keybord-input-not-work-in-chromium-34-ubuntu-14-04-aura-260972-using-fcitx-wo-449361.html

### Fazer Chromium ser mais parecido com o Uzbl
```chromium-browser --app=http://blog.fabricio.org```

### Extensions?
- https://chrome.google.com/webstore/detail/minimal-new-tab-clock/impmanfocmgfodfbnhbmkkonnpcogfak?hl=en
- https://chrome.google.com/webstore/detail/lubuntu-scrollbars/hemkkjpjknkkndhconammdhlhdkjclim/related?hl=en
- https://chrome.google.com/webstore/detail/penguinium/pkldogepcgpgphmkhenghhinknmopahp?hl=en

### Youtube?

#### Python pip
- http://www.saltycrane.com/blog/2010/02/how-install-pip-ubuntu/

```
sudo apt-get install python-pip python-dev build-essential
sudo pip install --upgrade pip
sudo pip install --upgrade virtualenv
```

#### youtube-dl
- http://www.uzbl.org/wiki/youtube-dl

```
sudo pip install --upgrade youtube_dl
```

- urls para testar:
  - https://twitter.com/Revision3/status/476082140493258754

### Facebook videos

- mesma url sem https e dominio downfacebook.com

## mplayer??
