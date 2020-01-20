# Priority

The priority icons are sorted by their priority

You don't actually need to set this value if you only have one priority icon



```yaml
  priority: 5
```

```yaml
  pri: 3
```

The larger the value, the earlier its requirement is checked

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

{% page-ref page="../../../actions/functional-actions/javascript.md" %}

