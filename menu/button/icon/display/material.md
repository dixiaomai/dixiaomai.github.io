---
description: Materials
---

# 材质

## **节点**

```javascript
material(s)?|id(s)?|mat(s)?
```

## 示例

```yaml
mats:
  # Original item
  - 'REDSTONE'
  # Player skull
  - '<head:Arasple>'
  # Player skull by variable
  - '<head:%player_name%>'
  # Custom texture skull
  - '<skull:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvYjU1MzE0MWFhYmU4OWE4YTU4MDRhMTcyMTMzYjQzZDVkMGVlMDU0OWNjMTlkYjAzODU2ODQwNDNjZmE5NDZhNSJ9fX0>'
  # Custom model data item (1.14+)
  - 'coal<model-data:COAL:1>'
```

```yaml
mats: 'REDSTONE'
```

## 玩家头颅

{% code title="Node" %}
```javascript
head|(player-)?head|(variable-)?head
```
{% endcode %}

```yaml
- '<player-head:playerID>'
- '<variable-head:playerID>'
- '<head:playerID>'
```

## 自定义纹理头颅

{% code title="Node" %}
```javascript
skull|custom(-head)?|custom(-skull)?
```
{% endcode %}

```yaml
- '<custom-head:TEXTURE>'
- '<custom-skull:TEXTURE>'
- '<skull:TEXTURE>'
```

{% embed url="https://minecraft-heads.com/custom-heads" %}

## 染色皮革

```yaml
- 'leather chestplate<dye:255,255,0>'

# RGB Color
```

## 自定义旗帜

```yaml
- 'white banner<banner:RED MOJANG,WHITE>'
```

{% embed url="https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/block/banner/PatternType.html" %}

## JSON Item \(NBT Support\)

```yaml
- '{"type":"DIAMOND_SWORD","data":0,"amount":1,"meta":{"Damage":{"type":"INT","data":0}}}'
```

通过命令 **/TrMenu Item** 转换物品为 JSON 文本   

## Head Database

需要插件 [https://www.spigotmc.org/resources/head-database.14280/](https://www.spigotmc.org/resources/head-database.14280/)

```yaml
- '<hdb:100>'
- '<head-database:100>'

- '<hdb:random>'
- '<head-database:random>'
```

## Oraxen

需要插件 [https://www.spigotmc.org/resources/72448/](https://www.spigotmc.org/resources/72448/)

```yaml
- '<oraxen:物品ID>'
```

