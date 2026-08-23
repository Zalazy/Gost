# GOST 一键脚本使用指南

致力于最简单好用的 GOST 小白脚本

## 启动脚本

### 国内机：

```bash
wget --no-check-certificate -O gost.sh https://gh-proxy.org/https://raw.githubusercontent.com/Zalazy/Gost/refs/heads/main/gost.sh && chmod +x gost.sh && ./gost.sh
```

### 国外机：

```bash
wget --no-check-certificate -O gost.sh https://raw.githubusercontent.com/huawuhen/Multi-EasyGost/master/gost.sh && chmod +x gost.sh && ./gost.sh
```

### 提示：

再次运行本脚本只需要输入 `bash gost.sh` 回车即可

* 注：由于 gost v2.11.2 功能稳定，此脚本将一直采用该版本，后续不再跟随官方更新

## 功能

### 原脚本功能

- 实现了systemd及gost配置文件对gost进行管理
- 在不借助其他工具(如screen)的情况下实现多条转发规则同时生效
- 机器reboot后转发不失效
- 支持传输类型：
  - tcp+udp不加密转发
  -  relay+tls加密

### 此脚本新增功能

- 增加了传输类型选择功能
* 新支持传输类型
  - relay+ws
  - relay+wss
- 落地机一键创建ss/socks5/http代理 (gost内置)
- 支持多传输类型的多落地简单型均衡负载
- 简单创建或删除gost定时重启任务
- 脚本自动检查更新
- 转发CDN自选节点ip
- 支持自定义tls证书，落地可一键申请证书，中转可开启证书校验
