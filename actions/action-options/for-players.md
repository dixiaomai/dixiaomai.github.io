---
description: Run the actions for all the online players
---

# For Players

## Aliases <a id="xie-fa"></a>

\(for\|all\)?\(-\)?players

```text
<PLAYERS:expression>
<ALL-PLAYERS:expression>

<PLAYERS> # No expression, for all online players
```

## Example <a id="shi-li"></a>

```yaml
# Send all online players a diamond
CONSOLE: give %player_name% diamond 1<Players>

# Kill online players that health is under 3.5
CONSOLE: kill %player_name%<Players: %player_health% <= 3.5>

# Broadcast a message
TELL: 你好啊<Players>
# Broadcast a Title
TITLE: <title=&a&lWow><Players>
```



