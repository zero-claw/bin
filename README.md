# bin

- zeroclaw multi-platform binary executable package 多平台二进制执行程序包

## 部署使用

- 运行环境
linux ubuntu 24.04

- 下载

```bash
wget https://raw.githubusercontent.com/zero-claw/bin/refs/heads/main/release/zeroclaw-ubuntu24.04-20260218.tgz
tar -xvf zeroclaw-ubuntu24.04-20260218.tgz
cp zeroclaw /usr/bin/
```
- 测试安装
zeroclaw --help
- 交互配置
zeroclaw onboard --interactive
生成配置文件并启动运行
~/.zeroclaw/config.toml
默认侦听端口127.0.0.0:3000
- 单次对话
zeroclaw agent -m "Hello, ZeroClaw!"

### 服务管理

- 安装服务
zeroclaw service install
- 启动服务
zeroclaw service start
- 查看服务
zeroclaw service status
systemctl --user status zeroclaw
- 设置自启动
systemctl --user enable zeroclaw
- 查看服务日志
journalctl --user -u zeroclaw

## ubuntu

### ubuntu 24.04

- [zeroclaw-ubuntu24.04-20260218](./release/zeroclaw-ubuntu24.04-20260218.tgz)
