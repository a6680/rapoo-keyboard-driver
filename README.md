# 雷柏键盘驱动程序

解决Liunx下ctrl和alt映射到了shift键位,导致无法正常使用

# 使用方法
```
git clone https://github.com/a6680/rapoo-keyboard-driver.git
cd rapoo-keyboard-driver
make
sudo make install
sudo bash install-rapoo-keyboard-driver.sh
```
# 注意
安装新内核（包含编译和安装内核）后，必须通过 “make&&sudo make install” 重新安装hid-rapoo模块。

# 错误1
```
rmmod: ERROR: Module hid_rapoo is not currently loaded
rmmod: ERROR: Module hid_generic is builtin.
modprobe: ERROR: could not insert 'hid_rapoo': Exec format error
```
# 错误2
```
rmmod: ERROR: Module hid_rapoo is not currently loaded
modprobe: ERROR: could not insert 'hid_rapoo': Operation not permitted
```
# 解决方法
#### 错误1
```
make clean
make
sudo make install
```
#### 错误2
关闭bios中到secure boot



