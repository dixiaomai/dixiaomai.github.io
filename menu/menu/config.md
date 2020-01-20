---
description: 本节将展示配置菜单的一些基本属性
---

# 配置菜单

## 提示

* 非必须项用 \* 标记, 可以不设置
* 该节所有配置内容需写入你创建的菜单 YAML 文件中

## Ⅰ. 设置菜单标题

```yaml
# 设置该容器的显示标题
Title: 'Hello, TrMenu'
```

暂时不支持动态标题

## Ⅱ. 设置容器类型

```yaml
Type: CHEST
```

配置此项，则 Shape 一项将无效

按钮的位置需要自行定义 Slot 属性

可用类型：

[https://bukkit.windit.net/javadoc/org/bukkit/event/inventory/InventoryType.html](https://bukkit.windit.net/javadoc/org/bukkit/event/inventory/InventoryType.html)

## Ⅲ.  **配置菜单排版**

```yaml
# 设置容器的页面排版
# *(一条字符串代表一行, 最多6行)
# *(单个符号代表一个按钮)
Shape:
  - '########C'
  - ' QTRMENU '
  - '   SAP   '
  - '         '
  - '#########'
```

通过模板，可以更直观、快速的设计菜单.

每个字符代表一个按钮，你在定义模板的同时也定义了容器大小

## Ⅳ. 开关条件 \*

```yaml
# (可选 | 默认无) 打开此菜单需要满足的条件表达式，需返回 Boolean 值
Open-Requirement: 'player.hasPermission("trmenu.use")'

# (可选 | 默认无) 若不满足打开此菜单需满足的条件, 则执行以下动作
Open-Deny-Actions:
  - 'tell: &7你缺少权限 &ctrmenu.use &7以打开此菜单.'

# (可选 | 默认无) 关闭此菜单需要满足的条件表达式，需返回 Boolean 值
Close-Requirement: null

# (可选 | 默认无) 若不满足关闭此菜单需满足的条件, 则执行以下动作 (不会阻止关闭菜单, 除非写打开动作)
Close-Deny-Actions: []
```

如果配置这些项，则玩家开启或关闭菜单需要满足这些表达式

注意，如果不满足关闭表达式，插件不会阻止玩家关闭该菜单，你需要在 Close-Deny-Actions 中写入重新打开本菜单的动作

## Ⅴ. 开关动作 \*

```yaml
# 定义开启菜单时的动作 (非必须项)
Open-Actions:
  - 'sound: BLOCK_CHEST_OPEN-1-2'
# 定义关闭菜单时的动作 (非必须项)
Close-Actions:
  - 'sound: BLOCK_CHEST_CLOSE-1-2'
```

这些是打开、关闭菜单后都会执行的动作

## Ⅵ. 菜单选项 & 绑定开启 \*

```yaml
# 菜单打开命令
Open-Commands:
  - 'example'
  - 'menu'

# 菜单选项 (非必须项, 不设置则使用默认值)
Options:
  # 菜单需要依赖的 PAPI 拓展名称, 若无将自动下载!
  # 我设计此功能是为了照顾小白服主
  Depend-Expansions:
    - 'server'
    - 'player'
    - 'progress'
    - 'math'
  # 是否在打开 GUI 时禁止玩家操作自己的背包? (默认:true)
  Lock-Player-Inv: true
  # 是否传递命令后面的参数? (可用 {N*} 来表示) (默认:false)
  Transfer-Args: false
  # 每天插件菜单刷新时，都将调用方法刷新玩家的背包
  # [!] 不推荐开启. 只有当你是低版本，且需要更流畅的动画更新效果时才有必要开启
  Update-Inventory: false
  # 强制传递参数的最小数量 (默认:0)
  Force-Transfer-Args: 0
  # 绑定物品打开 (下方需要需要识别的关键词Lore)
  Bind-Item-Lore:
    - '点击打开菜单'
```



