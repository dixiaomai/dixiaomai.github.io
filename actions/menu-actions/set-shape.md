---
description: Switch pages
---

# Set Shape

## Name

```text
((set|switch)(-)?shape)|shape
```

## Example

```yaml
- 'set-shape: 0'
```

* **0** means the first page
* You can also use variables in this action

```yaml
- 'set-shape: %math_{shape}-1%'
```

