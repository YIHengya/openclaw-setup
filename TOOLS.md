# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## What Goes Here

Things like:

- Camera names and locations
- SSH hosts and aliases
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## Examples

```markdown
### Cameras

- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH

- home-server → 192.168.1.100, user: admin

### TTS

- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

## QMD 本地搜索

- **索引**：`qmd collection add /path --name <name> --mask "*.md"`
- **更新索引**：`qmd update`
- **生成向量**：`qmd embed`（首次运行需要下载模型 ~330MB）
- **搜索**：`qmd query "关键词"`（需要下载 query expansion 模型 ~1.3GB）
- **简单搜索**：`qmd search "关键词"`（无需额外模型）
- **查看状态**：`qmd status`

当前已索引：workspace/*.md（8 个文件）

## 快速恢复

以后只需要说：**帮我配置 https://github.com/YIHengya/openclaw-setup**
