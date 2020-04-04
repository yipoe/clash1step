# clash1step
参照油管UP主：米月大佬灯脚脚本修改的一键安装Clash For Linux。自用。。。

# 只支持Debian 10.3（其他系统未测试）

## 脚本使用注意事项：

#### 脚本需要在root用户下执行，执行前需要自行创建一个非root用户供Clash安装跟运行

### 而且本方案使用的是Fake-ip的DNS模式，不喜勿用

### 安装完成后需手动上传yaml配置文件至：/home/用户名/.config/clash/

```
apt install wget -y
```

```
bash <(wget --no-check-certificate -qO- https://raw.githubusercontent.com/yuanlam/clash1step/test/clash1step)
```
Clash管理命令
```
systemctl restart clash.service      #重启

systemctl status clash.service      #查看状态

journalctl -u clash.service -f      #滚动实时状态
```

### 加入Smartdns和undound

SmartDNS管理命令
```
systemctl restart smartdns      #重启

systemctl status smartdns      #查看状态
```
unbound管理命令
```
systemctl restart unbound      #重启

systemctl status unbound      #查看状态
```

