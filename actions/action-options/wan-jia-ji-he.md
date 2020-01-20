---
description: 取在线玩家中符合条件的多个玩家，让他们都分别执行同一个动作
---

# 玩家集合

## 写法 <a id="xie-fa"></a>

\(for\|all\)?\(-\)?players

```text
<PLAYERS:表达式>
<ALL-PLAYERS:表达式>

<PLAYERS> # 全体玩家
```

## 示例 <a id="shi-li"></a>

```yaml
# 给全体在线玩家发一颗钻石
CONSOLE: give %player_name% diamond 1<Players>

# 杀死在线玩家中血量低于 3.5 的玩家
CONSOLE: kill %player_name%<Players: %player_health% <= 3.5>

# 向全体玩家发送一个公告
TELL: 你好啊<Players>
# 向全体玩家发送一个 Title 公告（Actionbar、Sound 等同样用法）
TITLE: <title=&a&lWow><Players>
```



