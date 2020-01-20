---
description: 必须满足此条件表达式要求时才会选用此图标
---

# 条件表达式

{% hint style="info" %}
**默认图标** 不需要条件表达式
{% endhint %}

每次按钮更新都将按优先级筛选满足自身条件表达式的图标用以展示

该表达式可以使用 PlaceholderAPI 变量以及 传递进来的参数，其编译结果**必须**是一个 **Boolean** 值.

## 示例

> "%player\_name%" == "Arasple"       当玩家名变量的字符串与 "Arasple" 匹配时为真
>
> player.hasPermission\("test"\)          当玩家拥有"test"权限时为真

支持使用的一些对象可以详细阅读 "脚本" 部分

```yaml
- condition: '"%player_name%" == "Arasple"'
```

{% page-ref page="../../../actions/functional-actions/jiao-ben.md" %}



