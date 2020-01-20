---
description: 菜单是由按钮构成
---

# 创建按钮

## 结构介绍

* 按钮主体
  * 更新周期
  * 优先级更新周期
  * 默认**显示模块**
  * 默认**动作模块**
  * 优先级图标
    * 图标1
      * 图标1 的**显示模块**
      * 图标1 的**动作模块**

## 示例按钮

```yaml
# 定义容器的按钮, 与 Shaple 模板中的字符相对应
# （可以二次定义动态位置）
BUTTONS:
  # 对应 Shape 中的模板排版中的字符
  '#':
    # (可选) 更新周期, 不设置则不刷新
    update: 25
    # (必须) 图标显示
    display:
      mats: GRAY_STAINED_GLASS_PANE
      name:
        - '&3Tr&bMenu'
        - '&3TrMenu'
      lore:
        - - '&7Tr&fMenu &7by &bArasple'
          - '&7Advanced & Dynamic menus for Minecraft'
        - - '&7Tr&fMenu &7by &2Arasple'
          - '&7Thanks for using :>'
    # 点击动作
    actions:
      # 类型 - [动作]
      all: ['sound: BLOCK_NOTE_BLOCK_PLING-1-2']
```

按钮稍后会详解

{% page-ref page="../button/" %}

