---
description: 图标是按钮的重要组成部分
---

# 图标

## 组成

TrMenu 的图标组成简单明了

* 条件表达式 \(默认图标不需要\)
* 显示部分
* 动作部分

```yaml
# 条件表达式部分（icons节点下的条件图标才需要, 按钮节点下的默认图标不需要）
- condition: '"%player_name%" == "Arasple"'
  # 显示部分
  display:
    mats:
      - 'REDSTONE'
    name: '&aName'
    lore:
      - ''
      - 'Lore'
      - ''
    # 动作部分
    actions:
      all:
        - 'close'
```

{% page-ref page="expression.md" %}

{% page-ref page="display/" %}

{% page-ref page="action.md" %}



