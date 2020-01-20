---
description: Materials
---

# Material

## **Node**

```javascript
material(s)?|id(s)?|mat(s)?
```

## Example

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

## Player's Skull

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

## Custom Texture Skull

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

Useful link

* [https://minecraft-heads.com/custom-heads](https://minecraft-heads.com/custom-heads)

## Dyed Leather Armor

```yaml
- 'leather chestplate<dye:255,255,0>'

# RGB Color
```

## Banner

```yaml
- 'white banner<banner:RED MOJANG,WHITE>'
```

[https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/block/banner/PatternType.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/block/banner/PatternType.html)

## Head Database

Require plugin [https://www.spigotmc.org/resources/head-database.14280/](https://www.spigotmc.org/resources/head-database.14280/)

```yaml
- '<hdb:100>'
- '<head-database:100>'

- '<hdb:random>'
- '<head-database:random>'
```

