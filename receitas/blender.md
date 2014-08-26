## Abrir o blender com medidas especificas no tamanho da janela (para screencast em HD)

./blender -p 0 0 1920 1080

## Dicas

### Evitar "fireflies"
- http://www.blenderguru.com/articles/7-ways-get-rid-fireflies/#.U_zJEB0b_mF
  - 


## Render farms

### Sheep-it
- https://www.sheepit-renderfarm.com
- download the jar file linked on the FAQ
  - https://www.sheepit-renderfarm.com/faq.php#commandline:
  -https://www.sheepit-renderfarm.com/media/applet/farm-client-3.2.1632.jar

```
java -cp farm-client-3.2.1632.jar com.renderfarm.worker.standalone.FermeDeRendu https://www.sheepit-renderfarm.com MYLOGIN MYPASSWORD
```

- cpulimit https://github.com/opsengine/cpulimit
- dicas p/ rodar na amazon http://blenderartists.org/forum/showthread.php?314856-Free-Render-Farm!/page2
- usar nice e renice p/ controlar a fritura de CPU
http://blender.stackexchange.com/questions/15247/how-to-configure-blender-so-that-it-uses-only-50-of-total-cpu-when-rendering

###
- http://blender.qarnot.net/
- pago
- bonito
- trial w/ free credits

### Blendergrid
- http://blendergrid.com/
- upload .blend, give your email and preferred time
- receive price in your email
