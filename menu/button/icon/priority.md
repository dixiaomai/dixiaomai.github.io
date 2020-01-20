# 优先级

条件图标是根据优先级大小来先后判断的

如果你只有一个条件图标，则不必设置此项

```yaml
  priority: 5
```

```yaml
  pri: 3
```

优先级数值越大，越先被检测条件是否满足

## 

```yaml
- condition: '"%player_name%" == "Arasple"'
  pri: 1
  display:
    mats: 'stone'
- condition: '"%player_name%" == "Bkm016"'
  pri: 2
  display:
    mats: 'diamond'
```

