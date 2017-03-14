# 遇到问题的解决方法

## ubuntu系统-problem
### 解决文本中文乱码(windows下文件)
* gsettings set org.gnome.gedit.preferences.encodings candidate-encodings "['UTF-8','GB18030','GB2312','GBK','BIG5','CURRENT','UTF-16']"
* #sudo apt-get install dconf-tools ->dconf-editor

### 更改软件源
vim /etc/apt/sources.list

### ubuntu16.04 连不了无线
具体解决方法：
  1. 右上角 System Setting -> System -> Software & Updates -> Additional Drivers
  2. 在等待一段时间之后，你会看到有几个选项搜索出来了，不过我就只有一个选项，这个选项默认是 Don't use the device 这个时候我们需要把它转换为：Using Processor ··· 也就是另外一个选项。
  3. 点击 Apply Changes 然后键入密码，系统自动开始安装一些程序.
  4. 重启电脑

  >* rfkill list all
  >* rfkill unblock all

## 软件-problem
### virtualbox
#### uuid already exists(插入vmdk时)
> VBoxManage internalcommands sethduuid <path of new vmdk>
```zsh
$ VBoxManage internalcommands sethduuid '/media/dr/软件/win7/win7.vmdk'
$ UUID changed to: 03048650-abc0-4c0c-817a-a22c0494c9d8
```