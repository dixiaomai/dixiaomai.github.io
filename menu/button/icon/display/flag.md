---
description: Item Flags
---

# 物品标签

## **节点匹配**

```javascript
flag(s)?
```

## 示例

```yaml
# 物品标签, 支持多个
flag:
- 'HIDE_ENCHANTS'
- 'HIDE_ATTRIBUTES'
```

可用标签：

> ```text
> HIDE_ENCHANTS - 隐藏附魔效果
> HIDE_ATTRIBUTES - 隐藏属性
> HIDE_UNBREAKABLE - 隐藏 “不可破坏” 描述
> HIDE_POTION_EFFECTS - 隐藏药水效果描述
> HIDE_DESTROYS - 隐藏破坏或修复
> HIDE_PLACED_ON - 隐藏放置描述
> ```



