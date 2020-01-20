---
description: Shiny
---

# 发光效果

## **节点匹配**

```javascript
shiny|glow
```

## 示例

```yaml
# 动态表达式决定, 需返回 Boolean 值
shiny: '%vault_eco_balance% >= 1000000'
```

```yaml
# 静态恒定
shiny: true
```

此效果为**真**时将自动为物品添加标签 **HIDE\_ENCHANTS**

