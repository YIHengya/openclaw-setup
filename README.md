# OpenClaw 快速恢复配置

> 复制下面的命令，在服务器上运行即可恢复完整配置

## 一键安装

```bash
# === 1. 安装 QMD（本地语义搜索）===
npm install -g @tobilu/qmd
qmd collection add /home/node/.openclaw/workspace --name workspace --mask "*.md"
qmd embed

# === 2. 安装 agent-reach（平台渠道）===
pip install https://github.com/Panniantong/agent-reach/archive/main.zip
agent-reach install --env=auto

# === 3. 验证安装 ===
mcporter list        # 查看 exa 搜索
agent-reach doctor   # 查看 agent-reach 状态
qmd status          # 查看 QMD 索引状态
```

---

## 快速恢复

以后只需要说：**帮我配置 https://github.com/YIHengya/openclaw-setup**

---

## 功能说明

| 功能 | 安装命令 | 用途 |
|------|----------|------|
| QMD | `npm install -g @tobilu/qmd` | 本地语义搜索，搜索 workspace 记忆 |
| agent-reach | `pip install ...` | Twitter/B站/YouTube/Reddit 等平台 |
| exa | 内置 via mcporter | 全网搜索 |

## 首次使用

1. 安装 CLI 工具
2. 配置 QMD 索引
3. 运行 `qmd embed` 生成向量（需下载 ~330MB 模型）
4. 可选：`qmd query` 需要额外 ~1.3GB 模型

## 磁盘空间

- QMD 模型：~2GB（embedding 330MB + query 1.3GB）
- 推荐：search 免费，query 按需安装

---

**发给我："帮我配置 https://github.com/YIHengya/openclaw-setup" 即可一键恢复**
