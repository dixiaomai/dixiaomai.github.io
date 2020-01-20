---
description: Amount
---

# 物品数量

## **节点匹配**

```javascript
amount(s)?
```

## 示例

```yaml
# 动态表达式数量, 需返回整数
amount: '%server_time_s%+1'
```

```yaml
# 静态恒定数量
amount: 5
```



