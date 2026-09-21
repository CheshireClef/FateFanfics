# AGENTS.md

## Cursor Cloud specific instructions

### 仓库性质
这是一个 **Obsidian 笔记库**（Fate 系列同人文写作存档，内容为中文 Markdown），不是软件工程项目。仓库中没有源代码、没有 `package.json` / `requirements.txt`，也**没有构建、测试或 lint 流程**。因此：
- 依赖刷新脚本为 no-op（无项目依赖需要安装）。
- 不存在 `build` / `test` / `lint` 命令；不要为其虚构测试。

### 目录结构
- `正文/`：已完成或连载中的正文。
- `大纲/`：故事大纲。
- `脑洞记录/`：未成形的点子记录。
- `.trae/documents/`：章节评估/优化清单。
- `README.md`：作品索引。

### 如何"运行"/预览
"应用"即 Obsidian 桌面程序，它只是渲染 Markdown 并用 git 做版本管理（内置社区插件 `obsidian-git`，已随库打包在 `.obsidian/plugins/`）。
- 桌面环境可用（`DISPLAY=:1`）。可下载 Obsidian AppImage（`obsidianmd/obsidian-releases`），用 `--appimage-extract` 解包后以 `obsidian --no-sandbox --disable-gpu` 启动。
- 首次打开某个库会弹出 "Do you trust the author of this vault?" 信任对话框；无需启用社区插件即可正常浏览/编辑（受限模式）。
- 也可用任意 Markdown 渲染器预览这些 `.md` 文件，效果等价。

### 注意事项（非显而易见）
- **`.obsidian/workspace.json` 会在 Obsidian 运行时被自动修改**（记录打开的标签页等 UI 状态）。它已被 git 跟踪，运行 Obsidian 后请勿把这类运行时改动提交进来——需要时用 `git checkout -- .obsidian/workspace.json` 还原。
- 文件名与内容大量使用中文和特殊符号（如 `【】`），处理路径时注意引号转义。
