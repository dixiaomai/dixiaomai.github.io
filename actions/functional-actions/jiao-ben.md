---
description: 执行一条脚本，支持使用一些对象
---

# 脚本

## 可用名称

* JS
* SCRIPT
* SCRIPTS
* JAVASCRIPT
* JAVASCRIPTS

## 写法

```
JS: player.sendMessage("Hello, " + player.getName())
```

## 可用对象

* player 玩家
* bukkitServer 服务器对象 （即 Bukkit.getServer\(\)）
* clickEvent 点击触发的事件
* clickType 点击类型
* clickItemStack 点击的物品

## 示例

```yaml
'B':
    update: 40
    display:
      mats:
      - 'apple'
      - 'beef'
      - 'cookie'
    actions:
      all:
      - 'js: bukkitServer.dispatchCommand(bukkitServer.getConsoleSender(), "give %player_name% " + clickItemStack.getType().name());'
```

动态展示一些食物，点击时给予该玩家正在展示的

