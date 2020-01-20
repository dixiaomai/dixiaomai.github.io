---
description: Slots
---

# 物品位置 \*

## **节点匹配**

```javascript
slot(s)?
```

## 示例

```yaml
# 动态多组位置, 写成 List<List<>>
slots:
  - [1, 2 , 3]
  - [4, 5, 6]
  - - 7
    - 8
    - 9
```

```yaml
# 静态多个位置
slots:
  - 1
  - 2
  - 3
```

{% hint style="info" %}
该项为非必选项, 默认通过模板中定位槽位, 设置此项后将覆盖模板中的定位
{% endhint %}

