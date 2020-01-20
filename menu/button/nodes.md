---
description: 快速配置你的按钮 & 图标
---

# 节点

## 示例按钮

```yaml
  'A':
    update: 20
    display:
      mats: '<head:%player_name%>'
      name:
        - '&6&lWelcome, &e&l%player_name%'
      lore:
        - - ''
          - '&7Some of your information'
          - ''
          - '&8▪ &7ID: &a%player_name%'
          - '&8▪ &7LEVEL: &3Lv.&b%player_level%'
          - '&8▪ &7FOOD: &6%player_food_level%'
          - ''
          - '&8▪ &7LOCATION: &2%player_world%, &b%player_x%/%player_y%/%player_z%'
          - ''
          - '&6&lHow about Left Click :>'
        - - ''
          - '&7Some of your information'
          - ''
          - '&8▪ &7ID: &a%player_name%'
          - '&8▪ &7LEVEL: &3Lv.&b%player_level%'
          - '&8▪ &7FOOD: &6%player_food_level%'
          - ''
          - '&8▪ &7LOCATION: &2%player_world%, &b%player_x%/%player_y%/%player_z%'
          - ''
          - '&f&lHow about Left Click :>'
      amount: '%server_online%'
    actions:
      all: ['sound: BLOCK_NOTE_BLOCK_PLING-1-2']
      left:
        - 'close'
        - 'title: <title=&a&lHello, &b&l%player_name%><subtitle=&7&lReady to fly...>'
        - 'wait: 25'
        - 'title: <subtitle=&6&l5s>'
        - 'wait: 20'
        - 'title: <subtitle=&3&l4s>'
        - 'wait: 20'
        - 'title: <subtitle=&b&l3s>'
        - 'wait: 20'
        - 'title: <subtitle=&2&l2s>'
        - 'wait: 20'
        - 'title: <subtitle=&a&l1s>'
        - 'wait: 20'
        - 'title: <subtitle=&6&lWoooooooo!>'
        - 'js: player.setVelocity(player.getVelocity().setY(15))'
        - 'js: player.setNoDamageTicks(20*10)'
    icons:
      - condition: '"%player_name%" == "Arasple"'
        display:
          name: '&2&lWelcome, &a&lAuthor!'
          lore:
            - ''
            - '&7Hello Arasple,'
            - '&7Woowwwwwww'
            - ''
```

## Ⅰ. 更新周期

按钮包括两个更新周期, 一是显示物品的刷新, 二是优先级图标的重新筛选

```yaml
# 刷新显示物品
update: 10
# 刷新优先级图标
refresh: 60
```

## Ⅱ. 默认图标

```yaml
# 默认显示部分
display:
  mats: ...
  name: ...
  lore: ...

# 默认动作部分
actions:
  # 类型 <-> [动作]
  all:
    - '...'
```

## Ⅲ. 条件图标

```yaml
icons:
  # 该条件图标的表达式
  - condition: '"%player_name%" == "Arasple"'
    priority: 0 
    # 该优先级图标的显示部分
    display:
      mats: ...
    # 该优先级图标的动作部分
    actions: ...
```

{% hint style="info" %}
优先级图标的显示部分的属性非必填，默认将继承默认图标的属性
{% endhint %}



