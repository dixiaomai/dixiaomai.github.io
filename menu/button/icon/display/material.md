---
description: Materials
---

# 物品材质

## **节点匹配**

```javascript
material(s)?|id(s)?|mat(s)?
```

## **示例**

```yaml
mats:
  # 原版物品的ID
  - 'REDSTONE'
  # 玩家ID头颅材质
  - '<head:Arasple>'
  # 玩家ID为变量的头颅材质
  - '<head:%player_name%>'
  # 自定义材质的头颅
  - '<skull:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvYjU1MzE0MWFhYmU4OWE4YTU4MDRhMTcyMTMzYjQzZDVkMGVlMDU0OWNjMTlkYjAzODU2ODQwNDNjZmE5NDZhNSJ9fX0>'
  # 自定义 Model Data 材质（1.14+）
  # 示例为 ModelData = 1 的 COAL 材质
  - '<model-data:COAL:1>'
```

```yaml
# 纯粹的静态单个物品材质
mats: 'REDSTONE'
```

## 正版玩家头颅

{% code title="节点匹配" %}
```javascript
head|(player-)?head|(variable-)?head
```
{% endcode %}

```yaml
# 以下列出多种写法, 节点忽略大小写
# 均支持使用变量、传入的参数

- '<player-head:头颅ID>'
- '<variable-head:头颅ID>'
- '<head:头颅ID>'
```

{% hint style="info" %}
TrMenu 的正版玩家头颅采用异步缓存为纹理形式的自定义头颅，杜绝卡顿现象 :\)
{% endhint %}

## 自定义纹理头颅

{% code title="节点匹配" %}
```javascript
skull|custom(-head)?|custom(-skull)?
```
{% endcode %}

```yaml
# 以下列出多种写法, 节点忽略大小写

- '<custom-head:头颅材质>'
- '<custom-skull:头颅材质>'
- '<skull:头颅材质>'
```

头颅材质需要为有效的 base64 值

* [https://minecraft-heads.com/custom-heads](https://minecraft-heads.com/custom-heads)

## 染色皮革

{% code title="节点匹配" %}
```javascript
<dye(-)?(leather)?:( )?([0-9]+[,]+[0-9]+[,]+[0-9]*>)
```
{% endcode %}

```yaml
- 'leather chestplate<dye:255,255,0>'

# RGB Color
```



## 自定义 Banner

{% code title="节点匹配" %}
```javascript
<banner(-)?(dye|color|style)?:( )?(.+>)
```
{% endcode %}

```yaml
- 'white banner<banner:RED MOJANG,WHITE>'
```

[https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/block/banner/PatternType.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/block/banner/PatternType.html)

## Head Database

需要安装插件 [https://www.spigotmc.org/resources/head-database.14280/](https://www.spigotmc.org/resources/head-database.14280/) 才能使用此功能

```yaml
# 引用 HeadDatabase 指定ID的物品
- '<hdb:100>'
- '<head-database:100>'
# 引用一个随机的 HeadDatabase 物品
- '<hdb:random>'
- '<head-database:random>'
```

