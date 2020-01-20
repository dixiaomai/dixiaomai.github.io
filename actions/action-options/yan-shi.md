---
description: 该动作延时执行，并继续执行剩下的动作
---

# 延时

## 写法 <a id="xie-fa"></a>

```text
<DELAY:延时>
<WAIT:延时>
```

## 示例 <a id="shi-li"></a>

```yaml
CONSOLE: give %player_name% diamond 1<Wait:60>

# 3s 后给予玩家一颗钻石
# 延时的单位是 Tick，20ticks = 1sec
```

{% hint style="info" %}
延时参数 是一个动作参数，仅针对该动作有效

而**延时动作**是一个**独立的动作，**会停止并等待一定时间后执行剩下的动作
{% endhint %}

