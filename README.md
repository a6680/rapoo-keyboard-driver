## 雷柏键盘驱动程序

解决Liunx下ctrl和alt映射到了shift键位,导致无法正常使用

### 使用方法
```
sudo apt install make gcc
git clone https://github.com/a6680/rapoo-keyboard-driver.git
cd rapoo-keyboard-driver
make
sudo make install
sudo bash install-rapoo-keyboard-driver.sh
```
## 注意
安装新内核（包含编译和安装内核）后，必须通过 “make&&sudo make install” 重新安装hid-rapoo模块。

## 运行错误1
```
rmmod: ERROR: Module hid_rapoo is not currently loaded
rmmod: ERROR: Module hid_generic is builtin.
modprobe: ERROR: could not insert 'hid_rapoo': Exec format error
```
解决方法
```
make clean
make
sudo make install
sudo bash install-rapoo-keyboard-driver.sh
```
## 运行错误2
```
rmmod: ERROR: Module hid_rapoo is not currently loaded
modprobe: ERROR: could not insert 'hid_rapoo': Operation not permitted
```
解决方法

关闭bios中的secure boot



