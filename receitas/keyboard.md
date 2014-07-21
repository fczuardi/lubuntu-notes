## Luz do teclado

```
echo 50 | sudo tee -a /sys/class/leds/smc::kbd_backlight/brightness
```

(substituindo 50 para um valor de 0 a 255)

## Acentos iguais ao do Mac (compose keys)

```
sudo dpkg-reconfigure keyboard-configuration
```
Macbookpro
Mac
English
(Altgr = dont use)
(compose = use right alt)

http://linux.m2osw.com/compose-key-under-linux
Chrome: https://bugs.launchpad.net/ubuntu/+source/chromium-browser/+bug/1309781

(mandinga: quit ibus e abre ibus-setup)
