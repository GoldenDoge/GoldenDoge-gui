# GoldenGoge-gui
GoldenDoge gui wallet 🐶

## About

Welcome to the repository of GoldenDoge gui wallet. Here you will find source code, instructions and wiki resources.

## How to build binaries from source code

### Windows
To build the gui you must have built GoldenDoge binaries, so please do all steps from [here](https://github.com/GoldenDoge/GoldenDoge#building-on-windows) and copy GoldenDoged.exe and walletd.exe from GoldenDoge/bin/Debug/ or GoldenDoge/bin/Release/ to GoldenDoge/bin/ before proceed. And you need to have GoldenDoge and GoldenDoge-gui folders in the same folder like /GDOGE/GoldenDoge and /GDOGE/GoldenDoge-gui Install [QtCreator](https://www.qt.io/download-thank-you?os=windows), open the project file GoldenDoge-gui/src/GoldenDoge-gui.pro in QtCreator and build it using MSVS kit (you must have MSVS installed already to build GoldenDoge binaries).

### Linux

```
# Install QtCreator and important packages:
$ sudo apt install qtcreator git cmake build-essential

$ wget -c 'http://sourceforge.net/projects/boost/files/boost/1.67.0/boost_1_67_0.tar.bz2/download'
$ tar xf download
$ rm download
$ mv boost_1_67_0 boost
$ cd boost
$ ./bootstrap.sh
$ ./b2 link=static -j 2 --build-dir=build64 --stagedir=stage
$ cd ..
$ git clone https://github.com/openssl/openssl.git
$ cd openssl
$ ./Configure linux-x86_64 no-shared
$ time make -j2
$ cd ..
$ git clone https://github.com/GoldenDoge/GoldenDoge
$ cd GoldenDoge
$ mkdir build
$ cd build
$ cmake ..
$ time make -j2
$ cd ../..
$ git clone https://github.com/GoldenDoge/GoldenGoge-gui
```
Now open the project file GoldenGoge-gui/src/GoldenGoge-gui.pro in QtCreator and build it.
