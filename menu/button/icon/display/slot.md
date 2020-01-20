---
description: Slots
---

# Slots \*

## Node

```javascript
slot(s)?
```

## Example

```yaml
# Animated slots, multiple slots
slots:
  - [1, 2 , 3]
  - [4, 5, 6]
  - - 7
    - 8
    - 9
```

```yaml
# Multiple slots, but do not change position
slots:
  - 1
  - 2
  - 3
```

{% hint style="info" %}
**Slots** are optional due to the defines of **Shape**
{% endhint %}

