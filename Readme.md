# How to build ffplay for linux
```
./configure --disable-asm --enable-small --disable-static --enable-shared --prefix=/usr/local --disable-ffmpeg --disable-ffprobe --disable-ffserver --disable-doc --disable-htmlpages --disable-podpages --disable-manpages --disable-txtpages --extra-ldflags=-lSDL_gfx
make
```
# How to build for miyoo
```
git clone https://github.com/MiyanoOsu/ffmpeg-miyoo.git
cd ffmpeg-miyoo
docker run --volume ./:/src/ -it miyoocfw/toolchain-shared-uclibc:latest
cd /src
./configure --disable-asm --enable-small --disable-static --enable-shared --prefix=/src/out/ffplay --disable-ffmpeg --disable-ffprobe --disable-ffserver --disable-doc --disable-htmlpages --disable-podpages --disable-manpages --disable-txtpages --extra-ldflags=-lSDL_gfx --enable-cross-compile --arch=arm --target-os=linux --cross-prefix=arm-linux- --pkg-config=/opt/miyoo/bin/pkg-config
make
make install
```
Then coppy all file in folder out/ffplay to /usr
