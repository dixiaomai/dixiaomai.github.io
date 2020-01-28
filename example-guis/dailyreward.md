# 每日礼包

## 目标效果

> 每 12h 可领取一次礼包, 菜单按钮显示 可领取 和 不可领取 两种不同状态的图标
>
> 要求动态显示还有多少 h, m, s 可领取礼包
>
> 音效、TITLE、不灵不灵的效果
>
> 每次领取全服通过 Actionbar 方式公告反馈
>
> 要求领取按钮能够到处跑

![](https://i.loli.net/2020/01/28/L35dM9AXU6ThSlk.gif)

## 准备

* TrMenu 1.15
* LuckPerms Bukkit 5.0.70
* PlaceholderAPI 2.10.4

需下载 LuckPerms 的 PlaceholderAPI 变量拓展 `/papi ecloud download LuckPerms` `/papi reload`

## 实现思路

这个相信大家都做过. 非常简单，优先级图标 + 临时权限，利用相关 PlaceholderAPI 变量 判断即可

## 配置

```yaml
TITLE:
- '每日礼包 DailyReward'
- '每日礼包 DailyReward'
- '每日礼包 DailyReward'
- 'Made by TrMenu, with &c❤'

TITLE-UPDATE: 40

OPEN-COMMANDS:
- '打卡'
- '(daily)?(-)?reward'

TYPE: HOPPER

BUTTONS:
  REWARD:
    update: 10
    refresh: 20
    display:
      mats: chest minecart
      # 调皮会跑的每日礼包
      slots: [
        [0],[1],
        [2],[2],[2],[2],[2],
        [2],[2],[2],[2],[2],
        [2],[2],[2],[2],[2],
        [3],[4]
      ]
      name: [
        '&b&l每&3日礼包 &7Daily-Reward',
        '&3每&b&l日&3礼包 &2Daily-Reward',
        '&3每日&b&l礼&3包 &7Daily-Reward',
        '&3每日礼&b&l包 &2Daily-Reward',
        '&3每日礼包 &7Daily-Reward',
      ]
      lore:
      - ''
      - '&7每隔 &e12h &7都可以白嫖一定的奖励,'
      - '&7还在犹豫什么? 狂点领取 !'
      - ''
      - '&f&o> &3点击即可白嫖'
    actions:
      all:
      - 'close'
      # 无敌二重奏
      - 'sound: UI_TOAST_CHALLENGE_COMPLETE-1-2'
      - 'sound: UI_TOAST_CHALLENGE_COMPLETE-1-0<delay:3>'
      # 标记临时权限 trmenu.dailyreward.claimed, 持续 12h
      - 'console: lp user %player_name% perm settemp trmenu.dailyreward.claimed true 12h'
      # 报喜
      - 'title: <TITLE=&a&l每日礼包><SUBTITLE=&3&l领取成功, 现已发放奖励>'
      - 'actionbar: &3沙雕玩家 &a{player_name} &3居然领取了每日礼包<players>'
      # 奖励内容 (下面可设置你自己的自定义奖励内容)
      # ...
    icons:
      - condition: '"%luckperms_expiry_time_trmenu.dailyreward.claimed%".length > 0'
        display:
          mats: minecart
          slots: [
            [0],[1],
            [2],[2],[2],[2],[2],
            [2],[2],[2],[2],[2],
            [2],[2],[2],[2],[2],
            [3],[4]
          ]
          lore:
          - ''
          - '&7你已经 &f白嫖 &7过了,'
          - '&7请等待冷却 ...'
          - ''
          - '&6&o> &c%luckperms_expiry_time_trmenu.dailyreward.claimed%'
```

