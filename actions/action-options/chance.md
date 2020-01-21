# Chance

## Aliases <a id="xie-fa"></a>

```text
<CHANCE:rate>
<RATE:rate>
```

## Example <a id="shi-li"></a>

```yaml
CONSOLE: give %player_name% diamond 1<Chance:0.55>
# 55% will give this player a diamond
```

```yaml
CONSOLE: clear %player_name% diamond 1<Require:"%checkitem_mat:diamond%" == "yes"><Chance:0.25>

# When the player has a diamond in his inventory,
# there is 25% chance will take one from him
```

​

