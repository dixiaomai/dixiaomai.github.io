---
description: 即设置菜单形状
---

# 切换菜单页码

## 节点

```text
((set|switch)(-)?shape)|shape
```

## 示例

```yaml
- 'set-shape: 0'
```

## 注意

形状的页码需是整数, 0 代表第一页

支持使用变量, 例如

```yaml
- 'set-shape: %math_{shape}-1%'
```

