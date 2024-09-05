# How to build ffplay for linux
```
./configure --disable-asm --disable-static --enable-shared --prefix=/usr/local --disable-ffmpeg --disable-ffprobe --disable-ffserver --disable-doc --disable-htmlpages --disable-podpages --disable-manpages --disable-txtpages --extra-ldflags=-lSDL_gfx
make
```
