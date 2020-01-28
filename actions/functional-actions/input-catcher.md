---
description: 对玩家输入的内容反应
---

# 输入捕获

## 节点

* CATCH
* CATCHER

## 示例

```yaml
- |-
  Catcher:
   <Type=CHAT>
   <Before=Tell: &3&lPlease type a value>
   <Valid=TELL:&6You typed a number &a$input>
   <Invalid=TELL:&cInvalid number input>
   <Require=TrUtils.isNumber("$input")>
   <Cancel=TELL:&7Canceld...>的
```

{% tabs %}
{% tab title="TYPE" %}
**CHAT**: 关闭玩家容器，拦截玩家下一次输入的聊天内容

**SIGN:** 给玩家发送一个虚拟木牌，等待编辑完成，读其中的内容
{% endtab %}

{% tab title="BEFORE" %}
当 Catcher 动作执行时首先执行的动作
{% endtab %}

{% tab title="VALID" %}
当有一个输入值并且输入值满足 Require （如果有）条件时
{% endtab %}

{% tab title="INVALID" %}
当有一个输入值并且输入值不满足 Require （如果有）条件时
{% endtab %}

{% tab title="CANCEL" %}
当输入捕获被取消时
{% endtab %}

{% tab title="REQUIRE" %}
可选，此项应是一个 JavaScript 表达式且返回布尔值类型

如果返回 false，即不满足，将会执行 Invalid 的动作并重新请求输入值

如果返回 true，即满足，将会执行 Valid 中的动作

**\[!\] 由于 &gt;, &lt; 等判断符号与该动作冲突，比较数值大小请调用 TrUtils 中的方法**
{% endtab %}
{% endtabs %}

上面不是所有的属性都是必须的，根据需要来

Catcher 是一个动作，利用 \|- 分行只是为了方便看，你也可以写一行

## 实例

TPA 请求

```yaml
      actions:
        all:
         - |-
            Catcher:
            <Type=SIGN>
            <Before=Tell:&3&l输入一个玩家的名称>
            <Valid=TELL:&3操作成功...;JS:player.chat("/tpa " + "$input")>
            <Invalid=TELL:&c玩家不在线>
            <Require=TrUtils.isPlayerOnline("$input")>
            <Cancel=TELL:&7取消操作>
```

