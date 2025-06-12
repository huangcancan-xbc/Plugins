# Obsidian 配置仓库

本目录包含 [Obsidian](https://obsidian.md/) 笔记软件的配置文件，用于快速同步个性化设置、插件和主题。适用于 `Software-Recommendations/obsidian` 笔记库。

## 📁 目录结构
```bash
.obsidian/
├── plugins/               # 已安装插件
│   ├── dataview/          # 示例：DataView 插件
│   └── ...              
├── themes/                # 自定义主题
│   └── my-custom-theme.css
├── snippets/              # CSS 片段
│   └── custom-admonitions.css
├── hotkeys.json           # 快捷键配置
├── app.json               # 核心设置（界面/编辑等）
└── community-plugins.json # 插件列表
```

## ✨ 功能特性
- **插件生态**：预配置生产力插件（如 Dataview、Templater 等）
- **主题优化**：包含暗色/亮色主题及 CSS 微调片段
- **模板系统**：预设常用笔记模板（需配合 Templater 插件使用）
- **自动化配置**：开箱即用的编辑器设置与快捷键方案

## 🛠️ 使用方法
1. **克隆本仓库**：
   ```bash
   git clone https://github.com/huangcancan-xbc/Software-Recommendations
   ```
2. **应用配置**：
   - 将本 `.obsidian` 文件夹复制到您的 Obsidian 库根目录
   - 启动 Obsidian → 信任此配置（首次使用时）

3. **插件激活**：
   - 进入 `设置 → 社区插件`，禁用安全模式
   - 逐个启用所需插件并配置

## ⚠️ 注意事项
- 覆盖现有配置前建议备份原 `~/.obsidian` 文件夹
- 部分插件需手动授权（如 Shell Commands）
- 主题文件可能需要安装 [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) 插件调整

## 🌟 推荐插件
| 插件名称 | 功能描述 | 配置文件路径 |
|---------|---------|-------------|
| Dataview | 自动化数据查询 | `plugins/dataview/` |
| Advanced Tables | 表格增强 | `plugins/advanced-tables/` |
| ... | ... | ... |

## 📜 许可证
本配置遵循 [MIT License](LICENSE)，包含的第三方插件/主题以各自原作者许可为准。
