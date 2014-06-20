## Install lubuntu

- mac iso
- pen drive boot app
- refit
- boot no live usb
- antes de fazer a instalacao selecione o additional drivers broadcom
- laptop plugado na internet via cabo
- instala
- se no boot ficar travado em um splash screen azul corrompido, reinicie e no grub escolha opcoes avancadas
- la, escolha o kernel mais antigo (general)
- se nao botar normal, tente colocar ```nouveau.noaccel=1```
- se bootar, va nos aditional drivers e escolha o driver proprietario nvidia mais recente (tested)
- reboot

## Ainda no LXDE

### Wifi

- no default LXSessions, Core Applications, em Network, preencha ```nm-applet```

## Instalar e Desinstalar coisas
- sudo apt-get install
- sudo apt-get autoremove
