# 配置菜单

## Ⅰ. 容器标题

```yaml
# 标题（静态）
Title: 'Hello, TrMenu'

# 标题更新周期（负数则不更新）
Title-Update: -1
```

```yaml
# 容器标题（动态）
Title:
  - 'Hello TrMenu'
  - 'This are animated titles,'
  - 'You can also use variables!'
  - 'Thx for using, %player_name%!'

# 更新周期（Ticks）
Title-Update: 40
```

## Ⅱ. 容器类型

```yaml
Type: CHEST
```

{% embed url="https://bukkit.windit.net/javadoc/org/bukkit/event/inventory/InventoryType.html" caption="可用类型" %}

## Ⅲ. 菜单形状

```yaml
# 快速排版菜单
# *(每个符号代表一个按钮)
Shape:
  - '########C'
  - ' QTRMENU '
  - '   SAP   '
  - '         '
  - '#########'
```

```yaml
# 多页菜单（多个形状）
Shape:
  - - '########C'
    - ' QTRMENU '
    - '   SAP   '
    - '         '
    - '########>'
  - - '#########'
    - ''
    - ''
    - '<########'
```

如果是箱子菜单，定义此项的同时也定义了菜单的大小

## Ⅳ. 开关条件动作

```yaml
# (Optional) 解读: 玩家拥有权限 trmenu.use 或打开方式是由 后台命令
Open-Requirement: 'player.hasPermission("trmenu.use") || "$openBy" == "CONSOLE"'

# (Optional)
Open-Deny-Actions:
  - 'tell: &7你需要权限 &ctrmenu.use &7打开此菜单.'

# (Optional)
Close-Requirement: null

# (Optional)
Close-Deny-Actions: []
```

## Ⅴ. 开关动作

```yaml
# (Optional) 当成功打开菜单时执行的动作
Open-Actions:
  - 'sound: BLOCK_CHEST_OPEN-1-2'
# (Optional)
Close-Actions:
  - 'sound: BLOCK_CHEST_CLOSE-1-2'
```

这些是打开、关闭菜单后都会执行的动作

## Ⅵ. 菜单选项 & 绑定开启

```yaml
# 绑定的开启命令
Open-Commands:
  - 'example'
  - 'menu'

# 菜单选项（全都是可选的，无需配置）
Options:
  # 本菜单强制需要以下 PlaceholderAPI 拓展，若无将自动下载
  Depend-Expansions:
    - 'server'
    - 'player'
    - 'progress'
    - 'math'
  # 锁定玩家背包 (Default: true)
  Lock-Player-Inv: true
  # 传参作为变量，第一个参数为 {0}, 第 N 个为 {N-1}
  Transfer-Args: false
  # 每次刷新图标时都更新玩家背包
  # [!] 不推荐开启. 除非你是低版本 Minecraft 服务器，且需要流畅的动画效果
  Update-Inventory: false
  # 强制需要的参数
  Force-Transfer-Args: 0
  # 绑定物品到指定的 Lore
  # 如下配置，则若某物品的 Lore 组中包括 OPEN_MENU, 玩家左右键交互将打开本菜单
  Bind-Item-Lore:
    - 'OPEN_MENU'
```



