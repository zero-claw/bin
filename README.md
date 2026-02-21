# bin

- zeroclaw multi-platform binary executable package 多平台二进制执行程序包

## 部署使用

- 运行环境
linux ubuntu 24.04

- 下载

```bash
wget https://raw.githubusercontent.com/zero-claw/bin/refs/heads/main/release/zeroclaw-ubuntu24.04-20260221.tgz
tar -xvf zeroclaw-ubuntu24.04-20260221.tgz
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

### 配对

- 注意：以网关或服务模式启动，默认必须配对才能连接
在启动日志或控制台输出中查看配对码

curl --request POST --url http://127.0.0.1:3000/pair -H 'X-Pairing-Code: 718820'

### 安全默认行为（关键）

- Gateway 默认绑定：`127.0.0.1:3000`
- Gateway 默认要求配对：`require_pairing = true`
- 默认拒绝公网绑定：`allow_public_bind = false`
- Channel allowlist 语义：
  - 空列表 `[]` => deny-by-default
  - `"*"` => allow all（仅在明确知道风险时使用）

## ubuntu

### ubuntu 24.04

- [zeroclaw-ubuntu24.04-20260221](./release/zeroclaw-ubuntu24.04-20260221.tgz)
- [zeroclaw-ubuntu24.04-20260220](./release/zeroclaw-ubuntu24.04-20260220.tgz)
- [zeroclaw-ubuntu24.04-20260219](./release/zeroclaw-ubuntu24.04-20260219.tgz)
- [zeroclaw-ubuntu24.04-20260218](./release/zeroclaw-ubuntu24.04-20260218.tgz)
