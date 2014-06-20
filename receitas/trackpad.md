## Configurar Lock Drag e Inverter Scroll com 2 dedos

- http://blog.mbirgin.com/?c=page&ID=550&t=lockeddragsclicklockinubuntulinux%  

```
$ xinput list
⎡ Virtual core pointer                    	id=2	[master pointer  (3)]
⎜   ↳ Virtual core XTEST pointer              	id=4	[slave  pointer  (2)]
⎜   ↳ bcm5974                                 	id=11	[slave  pointer  (2)]
⎣ Virtual core keyboard                   	id=3	[master keyboard (2)]
    ↳ Virtual core XTEST keyboard             	id=5	[slave  keyboard (3)]
    ↳ Power Button                            	id=6	[slave  keyboard (3)]
    ↳ Power Button                            	id=7	[slave  keyboard (3)]
    ↳ Sleep Button                            	id=8	[slave  keyboard (3)]
    ↳ Apple Computer, Inc. IR Receiver        	id=9	[slave  keyboard (3)]
    ↳ Apple, Inc. Apple Internal Keyboard / Trackpad	id=10	[slave  keyboard (3)]
```

- neste caso meu ID foi **11**

```
$ xinput list-props 11|grep Lock
    Synaptics Locked Drags (286):	1
    Synaptics Locked Drags Timeout (287):	5000
```

- neste caso o option id para Locked Drags foi **286**

```
$ xinput set-prop 11 286 1
```

### Inverter o scroll

- http://askubuntu.com/questions/205780/where-to-configure-synaptics-touchpad-to-use-inverted-two-finger-scrolling
- http://www.andybarratt.co.uk/lion-like-scrolling-on-ubuntu-inverse-scrolling-on-linux

(inverter 4 com 5 para vertical)
```
xinput set-button-map 11 1 2 3 5 4 6 7 8 9 10 11 12
```

#### 2 fingers horizontal scroll
- https://help.ubuntu.com/community/Lubuntu/Mouse#Touchpad_settings

```
synclient HorizTwoFingerScroll=1
```

(inverter 6 com 7 para horizontal)
```
xinput set-button-map 11 1 2 3 5 4 7 6 8 9 10 11 12
```

#### middle click with 3 fingers touch

- http://forums.linuxmint.com/viewtopic.php?f=49&t=108113
```
synclient TapButton3=2
```

#### mexer na sensibilidade

- muito util: http://uselessuseofcat.com/?p=74
- estava:

```
```
- ficou

```
```

Resumo: editar ~/.xinitrc para incluir:

```
xinput set-prop 11 286 1
xinput set-button-map 11 1 2 3 5 4 6 7 8 9 10 11 12
```

E depois no final de ~/.i3/config incluir:

```
exec ~/.xinitrc
```
