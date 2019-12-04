## install python2(aws ubuntu使用，是否通用未知)
#### ubuntu 16默认安装python3没有python2
```
sudo apt install python-minimal
```

## install opencv 3.4.0
### 安装依赖
```
sudo apt-get install build-essential
sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
```
### 安装opencv
```
wget https://github.com/opencv/opencv/archive/3.4.0.zip
unzip 3.4.0.zip
cd opencv-3.4.0
mkdir build
cd build
cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local ..
make
make install
```
### 调试
#### 如果调用报错，需要添加一下配置
```
sudo find / -name "libopencv_core.so.3.4*"
```
输出如下
```
/usr/local/lib/libopencv_core.so.3.4.0
/usr/local/lib/libopencv_core.so.3.4
```
将
```
/usr/local/lib/
```
添加到文件（不存在，新建这个文件）
```
/etc/ld.so.conf.d/opencv.conf
```
load config
```
sudo ldconfig -v
```
### 完成
