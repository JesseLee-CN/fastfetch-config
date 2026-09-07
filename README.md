# Fastfetch Theme · Windows

基于 [s0raLin/fastfetch-config](https://github.com/s0raLin/fastfetch-config) 适配 **Windows** 的融合版主题，在终端展示硬件 / 软件 / 桌面 / 运行信息，配 Windows 11 方块 Logo。

## 功能特点

- **硬件信息**：PC、CPU、GPU、RAM、硬盘、显示器
- **软件信息**：操作系统、内核、BIOS、包管理器、Shell
- **桌面信息**：窗口管理器、主题、终端、系统字体
- **系统信息**：开机时长、当前日期时间
- **终端配色**：Nerd Font 图标 + 16 色盘
- **Windows 11 Logo**：自定义 ASCII 实心方块，天蓝色

## Windows 专属改动（相对原主题）

| 项 | 说明 |
|---|---|
| 移除 `de` / `lm` | Linux 桌面环境 / Linux Mint 专属模块 |
| 移除 `OS Age` 命令 | 原为 `stat`/`date` 的 Linux 命令 |
| 增加 `Display` | 显示器分辨率 / 刷新率 |
| 增加 `Font` | 系统字体（Microsoft YaHei UI 等） |
| `logo.source` | 改用 `~/.config/fastfetch/ascii.txt`（Windows 下 `$HOME` 未定义） |
| `logo.color` | 自定义 Windows 蓝 `#4E87D0` |

> Linux 专属模块：`bios` / `wm` / `wmtheme` 在 Windows 上由 fastfetch 映射（DWM / 系统主题），均已保留。

## 安装方法

Windows 下将本仓库内容克隆到 fastfetch 的配置搜索目录（默认为 `~/.config/fastfetch`，即 `C:\Users\<你>\.config\fastfetch`）：

```powershell
git clone https://github.com/<你的用户名>/fastfetch-config-windows.git "$HOME\.config\fastfetch"
```

可直接运行验证：

```powershell
fastfetch
```

> 需要安装 Nerd Font（如 [CaskaydiaCove Nerd Font](https://www.nerdfonts.com/)）以正确显示图标；在 Windows Terminal 中设置字体后生效。

## 自定义

- 修改 `ascii.txt` 可更换顶部 Logo；配合 `config.jsonc` 中 `logo.color` 调整颜色（十六进制，如 `#4E87D0`）。
- 调整各模块图标、`keyColor`、`keyWidth` 与顺序，使其符合个人喜好。
- 增删模块见 `config.jsonc` 的 `modules` 数组（可用 `fastfetch --list-modules` 查看可用模块）。

## 基于

- [s0raLin/fastfetch-config](https://github.com/s0raLin/fastfetch-config)（原主题）
- [fastfetch-cli/fastfetch](https://github.com/fastfetch-cli/fastfetch)

喜欢的话给个 Star ✨
