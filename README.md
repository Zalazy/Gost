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

* 提示：

再次运行本脚本只需要输入 `bash gost.sh` 回车即可

> 注：由于 gost v2.11.2 功能稳定，此脚本将一直采用该版本，后续不再跟随官方更新

## 支持环境

| 项目 | 要求 |
| --- | --- |
| 最低支持系统 | Ubuntu 24.04+ / Debian 12+ |
| 推荐系统 | Ubuntu 24.04+ / Debian 12+ |
| 包管理器 | `apt-get` |
| 架构 | `x86_64` / `aarch64` |
| 引导方式 | 建议使用 GRUB |
| 使用场景 | VPS / 云服务器 / 独立服务器 |

不建议在树莓派、NanoPi 等依赖 U-Boot 或厂商定制内核链路的设备上使用。此类设备的内核安装和启动流程通常与通用 Debian/Ubuntu VPS 不一致。

Debian testing/unstable 如果缺少 `VERSION_ID`，脚本会按 `VERSION_CODENAME` 识别 `bookworm`、`trixie`、`forky` 和 `sid`。Alpine Linux 暂不支持安装本项目内核包，因为当前 release 产物是 `.deb`，安装和引导流程依赖 Debian/Ubuntu 的包管理与内核安装链路。

本项目当前内核主线为 Linux 7.x。安装内核时脚本会按最低支持系统拦截过旧环境，避免因用户态、initramfs 或引导链路过旧导致启动失败或 kernel panic。推荐系统是更稳妥的部署选择；旧系统仍可使用状态检查、网络调优、清空优化和卸载功能。
