# 技巧提示

## Boolean值 或 Yes/No 字符串无需额外判断

在使用变量表达式判断中，经常会遇到一些返回 true, false, yes 或 no 的变量

通常情况下判断应该是这样的

```yaml
- condition: '"%checkitem_mat:diamond%" == "yes"'
```

但是使用 TrMenu，只要返回 true, false, yes 或 no 字符串，都能自动转换为布尔类型值

这样简写即可

```yaml
- condition: '%checkitem_mat:diamond%'
```

## 非

使用 ! 前缀可以转换布尔值为其相反的

例如我们通过

{% tabs %}
{% tab title="判断有权限" %}
```yaml
- condition: 'player.hasPermission("demo")'
```
{% endtab %}

{% tab title="判断无权限" %}
```yaml
- condition: '!player.hasPermission("demo")'
```
{% endtab %}
{% endtabs %}

## 当变量只返回两个值时，没必要使用 2 个优先级图标

同样的，如 CheckItem 变量只返回 yes, no，你只需要一个优先级图标判断 yes 时

如果返回的 no, 则会显示默认图标，没必要再增加一个优先级图标来判断

## 相同条件需求的动作可以连在一起

例如你有一个很长的表达式，你需要满足该条件执行多个动作

可以用 \_\|\|\_ 

{% tabs %}
{% tab title="写法" %}
```yaml
- 'tell: Hello There<require: "%player_name%" == "Arasple" && player.getHealth()>20>'
- 'tell: I will give you a DIAMOND!<require: "%player_name%" == "Arasple" && player.getHealth()>20>'
- 'console: give %player_name% diamond 1<require: "%player_name%" == "Arasple" && player.getHealth()>20>'
```
{% endtab %}

{% tab title="简化" %}
```yaml
- |-
    <Require: "%player_name%" == "Arasple" && player.getHealth()>20>
    Tell: Hello There _||_
    Tell: I will give you a DIAMOND! _||_
    Console: give %player_name% diamond 1
```
{% endtab %}
{% endtabs %}

## 优先级图标可当优先级动作组使用

当你有复杂的动作组需求时，往往推荐你使用优先级图标

实际上，优先级图标完全不需要配置 显示部分，默认都将继承上级 默认图标

简化后的完成可以理解为优先级动作组！

```yaml
'A':
  display: #...
  actions: #...
  icons:
    - condition: 'condition1'
      actions:
      - 'action 1'
      - 'action 2'
```

## Options 的配置项都是可选的

菜单 Options 里面的配置项均可不配置，插件将使用默认值

## 



