# OpenClaw 快速恢复脚本

复制下面的命令，在服务器上运行即可：

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
