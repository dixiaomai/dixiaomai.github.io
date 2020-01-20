---
description: 一定概率执行此动作
---

# 概率

## 写法 <a id="xie-fa"></a>

```text
<CHANCE:概率>
<RATE:概率>
```

## 示例 <a id="shi-li"></a>

```yaml
CONSOLE: give %player_name% diamond 1<Chance:0.55>
# 55% 的概率给予该玩家一颗钻石
```

```yaml
CONSOLE: clear %player_name% diamond 1<Require:"%checkitem_mat:diamond%" == "yes"><Chance:0.25>

# 满足条件: 当玩家背包有钻石时
# 概率执行: 25% 的概率拿走一颗

# 需要 PlaceholderAPI 的 CheckItem 变量拓展
```

​

