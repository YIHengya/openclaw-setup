# OpenClaw 快速恢复指南

> 如果数据丢失，按以下步骤快速恢复

## 1. 全局 CLI 工具

```bash
# QMD - 本地语义搜索（必须从源码安装）
npm install -g @tobilu/qmd

# agent-reach - 平台渠道
pip install https://github.com/Panniantong/agent-reach/archive/main.zip
agent-reach install --env=auto

# xreach CLI（agent-reach 自带）
```

## 2. QMD 索引配置

```bash
# 初始化索引（首次）
qmd collection add /home/node/.openclaw/workspace --name workspace --mask "*.md"

# 生成向量（首次）
qmd embed

# 常用命令
qmd status              # 查看状态
qmd update              # 更新索引
qmd search "关键词"     # 关键词搜索
qmd query "语义"       # 语义搜索（需下载1.3GB模型）
```

## 3. mcporter 配置（已有）

```bash
mcporter list           # 查看已配置的 MCP 服务器
# exa 搜索已可用
```

## 4. 恢复搜索功能

```bash
# exa 搜索（免费，已配置）
mcporter call exa.web_search_exa query="你的问题" numResults=5

# 本地 QMD 搜索（workspace 记忆）
qmd search "关键词"
qmd query "语义"
```

## 5. 记忆文件位置

- Workspace: `/home/node/.openclaw/workspace/`
- 核心文件: `IDENTITY.md`, `USER.md`, `SOUL.md`, `AGENTS.md`, `TOOLS.md`
- 日常笔记: `memory/YYYY-MM-DD.md`

## 6. 常用命令

```bash
openclaw status              # 查看状态
openclaw gateway restart     # 重启 Gateway
agent-reach doctor          # 检查 agent-reach 状态
qmd status                  # 检查 QMD 索引状态
```

## 7. 注意事项

- QMD 需要 ~2GB 磁盘存储模型（embedding 330MB + query 1.3GB）
- search 免费，query 需要下载大模型
- agent-reach 部分渠道需要 Cookie 登录（建议用小号）
