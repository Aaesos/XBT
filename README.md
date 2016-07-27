# XBT
XBT is a high-performance, low overhead collection of bittorrent software. It is mainly comprised of XBTC, the client software, and of XBTT the tracker software.

XBTT is a pure BitTorrent tracker, written in C++. It is designed to offer high performance, while comsuming little resources. It is a pure tracker, so it doesn't offer a front end. I recommend XBTIT as a suitable front end, with built in support for XBTT.

## Getting Started
To use anything from this project, you are required to build it from source. To build this project, you will need the following dependencies.
To build on Debian, use this command.
```
apt-get install cmake g++ libboost-dev libmysqlclient-dev make git zlib1g-dev
```
To build on CentOS, Fedora Core, and Red Hat, use this command.
```
yum install boost-devel cmake gcc-c++ mysql-devel git
```

## Building the tracker
The following commands will clone, and build the tracker.
```
git clone https://github.com/Aaesos/XBT.git xbt
cd xbt
mkdir dist
cd tracker
./make.sh
mv xbt_tracker ../dist/xbt_tracker
cp xbt_tracker.conf.default ../dist/xbt_tracker.conf
```
You will find the tracker executable in xbt/dist. Starting it under linux is as simple as using the following command.
```
./xbt_tracker
```
If you are having troubles running it, ensure that the executable permission has been set. The following should fix the issue.
```
chmod 775 xbt_tracker
```
