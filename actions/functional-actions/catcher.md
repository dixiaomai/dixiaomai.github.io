---
description: 捕获玩家的输入内容并做出动作
---

# 捕获

## 可用名称

* CATCH
* CATCHER

## 写法

```yaml
- |-
  Catcher:
   <Type=CHAT>
   <Before=Tell: &3&lPlease type a value>
   <Valid=TELL:&6You typed a number &a$input>
   <Invalid=TELL:&cInvalid number input>
   <Require=TrUtils.isNumber("$input")>
   <Cancel=TELL:&7Canceld...>
```

{% tabs %}
{% tab title="TYPE" %}
获取玩家输入信息的方式

**CHAT**: 关闭菜单，等待玩家输入值到聊天中

**SIGN:** 创建一个虚拟木牌，等待玩家完成编辑
{% endtab %}

{% tab title="BEFORE" %}
当 Catcher 动作触发时最先执行的一个动作
{% endtab %}

{% tab title="VALID" %}
当有输入值且输入值满足 Require 条件时（如果有设置）执行的动作

（Catcher将关闭）
{% endtab %}

{% tab title="INVALID" %}
有输入值且输入值**不满足** Require 条件时执行的动作

（Catcher将重新等待输入）
{% endtab %}

{% tab title="CANCEL" %}
Catcher 被取消时执行的动作
{% endtab %}
{% endtabs %}



