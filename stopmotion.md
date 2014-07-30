
## Software

### Magic Lantern (para a camera)
- http://www.magiclantern.fm/
  - http://www.magiclantern.fm/install.html

### Darktable

- https://launchpad.net/~pmjdebruijn/+archive/darktable-release
  - https://launchpad.net/~pmjdebruijn/+archive/darktable-release

```
sudo add-apt-repository ppa:pmjdebruijn/darktable-release
sudo apt-get update
sudo apt-get install darktable
```

#### Darktable from git

- meu
```
git clone git://github.com/darktable-org/darktable.git
sudo apt-get install cmake
sudo apt-get install intltool
sudo apt-get install xsltproc
sudo apt-get install libxml2 libxml2-dev libxml2-utils  
sudo apt-get install webp
? sudo apt-get install libwebp-dev  
sudo apt-get install libgphoto2-dev
sudo apt-get install liblensfun-dev
sudo apt-get install librsvg2-dev
sudo apt-get install libsqlite3-dev
sudo apt-get install libexiv2-dev  
sudo apt-get install libcurl4-openssl-dev
sudo apt-get install liblcms2-dev
```

- do site
  - http://www.darktable.org/install/#source
```
sudo apt-get install intltool libatk1.0-dev libcairo2-dev libsoup2.4-dev libexiv2-dev libfontconfig1-dev libfreetype6-dev libgomp1 libgtk2.0-dev libjpeg-dev libtiff4-dev liblcms2-dev liblensfun-dev libpng12-dev libsqlite3-dev libstdc++6-4.4-dev libxml2-dev libopenexr-dev libcurl4-gnutls-dev libgphoto2-2-dev libdbus-glib-1-dev libgnome-keyring-dev fop librsvg2-dev libflickcurl-dev cmake liblua5.2-dev libcolord-dev
```

e
```
 sudo apt-get install openjdk-7-jdk
```

### Youtube
- https://support.google.com/youtube/answer/1722171

### VP8
- http://wiki.webmproject.org/howtos/convert-png-frames-to-webm-video
```
sudo apt-get install vpx-tools
```

#### YUV
- http://wiki.webmproject.org/howtos/convert-png-frames-to-webm-video

```
png2yuv -I p -f 24 -b 1 -n 1440 -j %04d.png > input_3840x2160_24fps.yuv
```

#### VP8

- http://www.webmproject.org/tools/encoder-parameters/#10-sample-command-lines
- https://support.google.com/youtube/answer/1722171?hl=en

1920_1080

png2yuv -I p -f 24 -b 1 -n 781 -j preview%04d.png > input_1920_1080_24fps.yuv
(781 eh o numero de frames)

vpxenc  input_1920_1080_24fps.yuv -o outputb_vp8_1920x1080_24fps.webm \
  --codec=vp8 --i420 -w 1920 -h 1080 -p 2 -t 4 \
  --good --cpu-used=0 --target-bitrate=8000 --end-usage=vbr \
  --auto-alt-ref=1 --fps=24000/1001 -v \
  --minsection-pct=5 --maxsection-pct=800 \
  --lag-in-frames=16 --kf-min-dist=0 --kf-max-dist=360 \
  --token-parts=2 --static-thresh=0 --drop-frame=0 \
  --min-q=0 --max-q=60

2-Pass Faster VBR Encoding

3840x2160

vpxenc  input_3840x2160_24fps.yuv -o output_vp8_3840x2160_24fps.webm \
  --codec=vp8 --i420 -w 3840 -h 2160 -p 2 -t 4 \
  --good --cpu-used=0 --target-bitrate=45000 --end-usage=vbr \
  --auto-alt-ref=1 --fps=24000/1001 -v \
  --minsection-pct=5 --maxsection-pct=800 \
  --lag-in-frames=16 --kf-min-dist=0 --kf-max-dist=360 \
  --token-parts=2 --static-thresh=0 --drop-frame=0 \
  --min-q=0 --max-q=60


##### add Audio

```
(exportar do blender p/ flac)
ffmpeg -i ../preview2.flac -acodec libvorbis -ab 384k ../preview2.ogg
sudo apt-get install mkvtoolnix
mkvmerge --webm -o combined.webm video.webm audio.ogg
```

### Daala

- https://wiki.xiph.org/Daala_Quickstart

```
git clone https://git.xiph.org/daala.git
cd daala
./autogen.sh
./configure --disable-unit-tests
make
...

checking for SDL... no
configure: error: Package requirements (sdl) were not met:

No package 'sdl' found

Consider adjusting the PKG_CONFIG_PATH environment variable if you
installed software in a non-standard prefix.

Alternatively, you may set the environment variables SDL_CFLAGS
and SDL_LIBS to avoid the need to call pkg-config.
See the pkg-config man page for more details.
```

```
sudo apt-get install libsdl1.2-dev
sudo apt-get install libogg-dev
make
```

#### PNG > YUV
```
./tools/png2y4m video%05d.png -o video.y4m
```

#### related bookmarks
- http://maikmerten.livejournal.com/4487.html
- https://media.xiph.org/video/derf/
- http://lists.xiph.org/pipermail/daala/2014-May/000030.html

### FFMPEG

```
sudo add-apt-repository ppa:jon-severinsson/ffmpeg
sudo apt-get update
sudo apt-get install ffmpeg
```

### Blender

- http://wiki.blender.org/index.php/Doc:2.6/Manual/Preferences/Input
  - User preferences > Input

- http://eugenia.queru.com/2008/04/20/video-editing-with-blender/
  - tem um preset de UI para video editing

- Webm
  - http://wiki.webmproject.org/howtos/convert-png-frames-to-webm-video

- 2 transform p/ scale + pan
  - http://blender.stackexchange.com/questions/6712/how-to-shrink-an-image-with-the-video-sequence-editor

#### Melt
-
- https://www.youtube.com/playlist?list=PLcUid3OP_4OWC-GJ6KfHK7dIK_yRKKn0e

### KDEnLive
```
sudo apt-get install kdenlive
```

Para tema escuro:

- http://forum.kde.org/viewtopic.php?f=269&t=114184
  - "Wonton Soup"
  - http://kde-look.org/content/show.php/Wonton+Soup+Neutral?content=148680
```
sudo apt-get install systemsettings
```
- copiar do systemsettings para qtconfig-qt4 as cores manualmente :(

### flowblade
- https://code.google.com/p/flowblade/

### Shotcut
- http://www.shotcut.org/bin/view/Shotcut/Download

```
sudo apt-get install libqt5webkit5-dev
sudo apt-get install libqt5x11extras5-dev
sudo apt-get install libmlt-dev
?sudo apt-get install libqt5widgets5
```




### Lightworks

- http://www.lwks.com/

### Ardour
- http://ardour.org/

### PiTiVi
-
```
sudo apt-get install pitivi
```

- falhou:
  - tentei http://fundraiser.pitivi.org/download-bundles



### Cinelerra

- http://www.g-raffa.eu/Cinelerra/HOWTO/installation.html
```
sudo apt-add-repository ppa:cinelerra-ppa/ppa
sudo apt-get update
sudo apt-get install cinelerra-cv
```

- image sequence
  - http://www.g-raffa.eu/Cinelerra/HOWTO/animations.html


### Openshot

```
sudo apt-get -f install
sudo apt-get install openshot
```
