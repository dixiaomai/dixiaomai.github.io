---
description: 为了方便不熟悉的服主快速入门，本节只提供几个常用的表达式模板供参考
---

# 条件

## 准备

为了充分发挥表达式判断的强大优势，需要安装一些相关的 PlaceholderAPI 拓展

可以在这里查询

{% embed url="https://github.com/PlaceholderAPI/PlaceholderAPI/wiki/Placeholders" %}

## Ⅰ. 权限判断

```javascript
player.hasPermission("default.user")

# 玩家是否有权限 "default.user", 有则返回 true, 注意需用引号
```

{% code title="实例" %}
```yaml
- 'Console: give %player_name% diamond 1<Requirement:player.hasPermission("user.vip")>'

# 当玩家有 user.vip 节点权限时，通过后台执行命令，分发一个钻石
```
{% endcode %}

## Ⅱ. 数值变量判断

```yaml
player.getHealth() >= 20 # 当玩家血量大于等于 20 返回 true
%player_health% < 15 # 当玩家血量小于 15 返回 true, (这里是用 PAPI 变量的)
```

```yaml
%server_tps% < 18 # 服务器 TPS 小于 10 时返回 true 
```

## Ⅲ. 字符串变量的判断

常量、PlaceholderAPI 变量 需要用双引号引起来

```yaml
player.getName() == "Arasple" # 当玩家名称为 Arasple 时返回 true

"%checkitem_mat:diamond,amt:5%" == "yes"
# 利用 CheckItem 变量，判断玩家至少有 5 颗钻石时，返回 true
# 因为该变量本身的返回值是 "yes" 和 "no"
```



