# 果汁搜盘 Web（juicePans-web）

> **姊妹项目**：若需要 **AI Skill / 命令行** 搜索，请使用 [juicePans](https://github.com/sxsxhhh/juicePans)。本仓库是独立的 **浏览器本地 / Docker Web 站点**。

本地浏览器搜盘站点：多引擎聚合搜索、链接存活检验、可选 Docker 部署。解压绿色版或源码启动后，在浏览器里搜索网盘公开分享链接。

## 这是什么

- 多盘种并行搜索、去重与相关度排序
- 「检验链接存活」开关；搜索过慢时可终止
- 绿色版：解压即用（需本机 Python 3.8+）
- Docker：`web/` 目录一键构建运行（端口默认 `8765`）

本工具**只检索、展示**公开分享链接，不托管、不转存文件。

## 快速开始

### 绿色版

1. 在 [Releases](https://github.com/sxsxhhh/juicePans-web/releases) 下载 `*-web-green.zip`
2. 解压后 Windows 双击 `start.bat`（或其他系统执行 `bash start.sh` / `python3 server.py`）
3. 浏览器打开 `http://127.0.0.1:8765/`

详细步骤见 [docs/deploy-green.md](docs/deploy-green.md)。

### 源码本地运行

```bash
git clone https://github.com/sxsxhhh/juicePans-web.git
cd juicePans-web/web
python3 server.py
```

见 [docs/deploy-local.md](docs/deploy-local.md)。

### Docker

```bash
git clone https://github.com/sxsxhhh/juicePans-web.git
cd juicePans-web/web
docker compose up -d --build
```

见 [docs/deploy-docker.md](docs/deploy-docker.md)。

## 项目结构

```text
juicePans-web/
├── web/                 # 站点源码、Dockerfile、docker-compose
├── docs/
│   ├── deploy-green.md
│   ├── deploy-local.md
│   └── deploy-docker.md
└── README.md
```

## 环境变量

| 变量 | 说明 |
|------|------|
| `JUICEPANS_HOST` | 监听地址，局域网访问设为 `0.0.0.0` |
| `JUICEPANS_PORT` | 端口，默认 `8765` |

## 与 juicePans Skill 的关系

| | [juicePans](https://github.com/sxsxhhh/juicePans) | 本仓库 juicePans-web |
|--|--|--|
| 形态 | AI Skill + CLI | 浏览器本地 / Docker 站点 |
| 典型用法 | 对话安装 skill，或 `python scripts/search.py` | 绿色版 / `server.py` / Docker |
| 是否转存 | 否 | 否 |

## 许可证

与 juicePans 一致，采用 **GNU GPL-3.0**。完整文本见 [LICENSE](LICENSE)。

## 免责声明

仅供学习研究；不存储、不传播资源文件；搜索结果版权归原作者 / 版权方。请支持正版。
