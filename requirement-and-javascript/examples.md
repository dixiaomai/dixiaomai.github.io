# Requirements

## Get Ready

Expressions always require a lot of PlaceholderAPI variables in order to fulfill powerful features 

So you'd better download the Cloud Expansions you need.

The link below is where you can find the variables

{% embed url="https://github.com/PlaceholderAPI/PlaceholderAPI/wiki/Placeholders" %}

## Ⅰ. Permission Check

```javascript
player.hasPermission("default.user")
```

## Ⅱ. Numbers Check

```yaml
player.getHealth() >= 20
%player_health% < 15
```

```yaml
%server_tps% < 18
```

## Ⅲ. String equals

**Note: " " is necessary**

```yaml
player.getName() == "Arasple"
"%checkitem_mat:diamond,amt:5%" == "yes"
```



