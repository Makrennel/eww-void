## Elkowars Wacky Widgets (EWW) for Void Linux

This repository contains template files for building [eww](https://github.com/elkowar/eww) using xbps-src.

### Usage

1) You may want to start by making a directory where you can keep the relevant repositories

```
$ mkdir ~/repos
$ cd ~/repos
```

2) Set up a [void-packages](https://github.com/void-linux/void-packages) clone for building templates files

```
$ git clone https://github.com/void-linux/void-packages
$ cd void-packages
$ ./xbps-src binary-bootstrap
$ cd ..
```

3) Clone this repository:

```
$ git clone https://github.com/Makrennel/eww-void.git
$ cd eww-void
```

4) Copy srcpkgs to your void-packages srcpkgs directory

```
$ cp -r srcpkgs/* ../void-packages/srcpkgs
```

5) Build and install eww

```
cd ../void-packages
$ ./xbps-src pkg eww
$ sudo xbps-install -R hostdir/binpkgs eww
```

Note: The `eww` package contains the binaries for both the wayland and x11 versions, which must be run as `eww-wayland` or `eww-x11`.
