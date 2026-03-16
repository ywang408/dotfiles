# niri 模块化配置（按你当前需求）

这个目录已经把你提到的组合放好：

- Noctalia launcher
- Vivaldi 主浏览器（`vivaldi-stable`）
- Papers
- Nautilus
- foot
- 1Password
- 科研 / 多窗口工作区分配方案（见 `WORKSPACE_PLAN.md`）

## 目录结构

```text
niri/
├── config.kdl
├── WORKSPACE_PLAN.md
└── cfg/
    ├── autostart.kdl
    ├── keybinds.kdl
    ├── input.kdl
    ├── display.kdl
    ├── layout.kdl
    ├── rules.kdl
    ├── misc.kdl
    └── local.kdl
```

## 使用方式

1. 备份你现有配置：
   ```bash
   cp -a ~/.config/niri ~/.config/niri.bak.$(date +%F-%H%M%S)
   ```
2. 拷贝到家目录：
   ```bash
   mkdir -p ~/.config/niri
   cp -a ./niri/* ~/.config/niri/
   ```
3. 重载 niri 配置（在会话内执行）：
   ```bash
   niri msg action reload-config
   ```

## 备注

- `cfg/local.kdl` 预留给“这台机器专属”的临时/覆盖配置，后续调显示器、灵敏度建议都写这里。
- 如果遇到需要管理员权限但没有认证弹窗，可在 `cfg/autostart.kdl` 里启用 polkit agent 那行。
