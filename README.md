# Claude Code Here - 右键菜单集成

在 Windows 资源管理器的文件夹右键菜单中添加 "Claude Code Here" 选项，快速在指定目录打开 Claude Code。

## 功能

- **文件夹右键菜单**：在任意文件夹上右键 → `Claude Code Here`，会在该目录下打开 cmd 并启动 Claude Code
- **文件夹空白处右键菜单**：在文件夹空白区域右键 → `Claude Code Here`，会在当前目录下打开 cmd 并启动 Claude Code
- 支持含空格的路径和 UNC 网络路径

## 安装

1. **以管理员身份运行** `install.reg`：
   - 双击 `install.reg` 文件
   - 在弹出的用户账户控制 (UAC) 对话框中点击 "是"
   - 在注册表编辑器警告对话框中点击 "是" 确认导入

2. 或者使用命令行：
   ```cmd
   reg import install.reg
   ```

## 卸载

1. **以管理员身份运行** `uninstall.reg`：
   - 双击 `uninstall.reg` 文件
   - 在弹出的用户账户控制 (UAC) 对话框中点击 "是"
   - 在注册表编辑器警告对话框中点击 "是" 确认导入

2. 或者使用命令行：
   ```cmd
   reg import uninstall.reg
   ```

## 注册表位置

| 功能 | 注册表路径 |
|------|-----------|
| 文件夹右键菜单 | `HKEY_CLASSES_ROOT\Directory\shell\ClaudeCodeHere` |
| 文件夹空白处右键菜单 | `HKEY_CLASSES_ROOT\Directory\Background\shell\ClaudeCodeHere` |

## 注意事项

- 需要已安装 Claude Code CLI 工具（`claude` 命令可用）
- 导入 `.reg` 文件需要管理员权限
- 安装/卸载后右键菜单会立即生效，无需重启资源管理器
- `uninstall.reg` 使用 `[-]` 前缀删除整个注册表键及其所有子键
