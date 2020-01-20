---
description: 玩家必须满足表达式条件才能执行此动作
---

# 条件

## 写法

```text
<REQUIRE:表达式>
<REQUIREMENT:表达式>
<CONDITION:表达式>
```

当表达式内容返回 true 时，则执行该动作，否则不执行

## 示例

```yaml
TELL: You're so poor <Require:%vault_eco_balance_fixed% <= 100>

# 只有当该名玩家的余额<=100时，才执行这条动作(即发送 "You're so poor")
# 因为通过 PlaceholderAPI 的 Vault 变量判断，需要确保安装该变量拓展以及所需环境
```



