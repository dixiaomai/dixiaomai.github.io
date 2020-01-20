---
description: 了解 TrMenu 的配置结构
---

# 配置

## 文件目录

| 文件（目录） | 描述 |
| :--- | :--- |
| settings.yml | 主配置文件 |
| lang/zh\_CN.yml | 语言文件 |
| menus | 菜单目录 |

{% hint style="success" %}
TrMenu 所有配置文件均会监听文件改动，自动重载
{% endhint %}

## 配置文件

{% code title="settings.yml" %}
```yaml
################################################################################
#
#  ____________________   _____  __________________   ____ ___
#\__    ___\______   \ /     \ \_   _____/\      \ |    |   \
#  |    |   |       _//  \ /  \ |    __)_ /   |   \|    |   /
#  |    |   |    |   /    Y    \|        /    |    |    |  /
#  |____|   |____|_  \____|__  /_______  \____|__  |______/
#                  \/        \/        \/        \/
#
# 高级动态菜单插件
#
# https://github.com/Arasple/TrMenu
#
################################################################################
CONFIG-VERSION: 0

# 相关选项
OPTIONS:
  # 原版材质读取时智能相似度识别最小百分比
  MATERIAL-SIMILAR-DEGREE: 0.8
  # 最小的点击延时, 防容器点击事件刷屏 (ms)
  ANTI-CLICK-SPAM: 200
  # 是否启用菜单自动重载
  # * 插件将对已载入的菜单文件监听文件改动
  # * 并自动重载, 包括刷新已打开的菜单
  # * 如果有任何错误发生则不通知、重载
  MENU-FILE-LISTENER:
    # 是否启用
    ENABLE: true
    # 成功的加载是否通知控制台
    NOTIFY: true

# 自定义路径载入菜单
# (plugins/TrMenu/menus 目录及其子目录下的菜单默认均会加载)
MENU-FILES:
  - 'plugins/XXX/zzz.yml'

# 内置菜单
MENUS:
  - internalMenu:
      title: 'Internal Menu in settings.yml'
      shape:
        - '#########'
        - '    |    '
        - '#########'
      buttons:
        '#':
          display:
            mats: green stained glass pane
        '|':
          display:
            mats: apple
            name: '&6Nice to meet you~'
```
{% endcode %}

## 语言文件

{% code title="zh\_CN.yml" %}
```yaml
PLUGIN:
  LOADING:
    - ''
    - '&3Tr&bMenu &7正在载入中...'
    - ''
  ENABLED: '&8[&3Tr&bMenu&8] &bINFO &8| &3加载完毕. TrMenu &av{0} &3现已启用, 敬请使用.'
  DISABLED: '&8[&3Tr&bMenu&8] &bINFO &8| &7感谢使用本插件, 您在论坛为本插件评分即是对作者最大的鼓励!'
  DEPEND:
    DOWNLOAD: '&8[&3Tr&bMenu&8] &eDEPEND &8| &7正在下载前置插件 &f{0} &7...'
    INSTALL: '&8[&3Tr&bMenu&8] &eDEPEND &8| &7已成功下载前置 &3{0} &7, 即将重启服务端完成安装...'
    INSTALL-FAILED: '&8[&3Tr&bMenu&8] &eDEPEND &8| &7自动下载前置 &c{0} &7过程出错, 请手动安装, 服务器即将停止...'
  HOOKED: '&8[&3Tr&bMenu&8] &eDEPEND &8| &7成功检测并挂钩软依赖插件 &6{0}&7...'
  UPDATE-NOTIFY:
    LATEST: '&8[&3Tr&bMenu&8] &2你正在运行最新版的 &3TrMenu&a.'
    DEV: '&8[&3Tr&bMenu&8] &6你正在运行开发版本的 TrMenu, 请及时反馈漏洞!'
    TOO-OLD:
      - "&8--------------------------------------------------"
      - "&r"
      - "&8# &4您所运行的 &cTrMenu &4版本过旧, 可能潜在很多漏洞"
      - "&8# &4请及时更新到最新版本以便获得更好的插件体验!"
      - "&8# &r"
      - "&8# &4Mcbbs: &chttps://www.mcbbs.net/thread-918078-1-1.html"
      - "&8# &r"
      - "&8# &r"
      - "&8# &4服务器将在 &c&l{0} secs &4后继续启动..."
      - "&r"
      - "&8--------------------------------------------------"
    HEADER:
      - ''
      - '§3--------------------------------------------------'
      - '&7▪ &3TrMenu &a更新通知 &8{0} &7➦ &8{1}'
      - ''
      - '&7▪ &e内容: '
    FOOTER:
      - ''
      - '&7▪ &2Github下载: &a&nhttps://github.com/Arasple/TrMenu/releases/latest'
      - '§3--------------------------------------------------'

ERROR:
  HDB: '&8[&3Tr&bMenu&8] &cERROR &8| &c未安装 &6HeadDatabase&c, 你无法使用该材质: &6{0}'
  VERSION: '&8[&3Tr&bMenu&8] &cERROR &8| &7检测版本号时发生异常... 关闭服务器!'
  JS:
    - '&8[&3Tr&bMenu&8] &cERROR &8| &c表达式计算时出错: &2{0}'
    - '&6{1}'
    - '&8{2}'

CONVERTER:
  CHESTCOMMANDS: '&8[&3Tr&bMenu&8] &aSUCCESS &8| &7检测并成功转换导入 &3{0} &7个 &6ChestCommands &7菜单... &8(仅转换基础布局)'

MENU:
  LOADED-AUTOLY: '&8[&3Tr&bMenu&8] &bINFO &8| &7监听到文件改动并自动成功重载了菜单 &f{0}&7...'
  LOADED-AUTOLY-FAILED: '&8[&3Tr&bMenu&8] &6WARN &8| &7自动重载菜单 &f{0} &7的过程中出错, 菜单更新失败, 请检查错误重新编辑保存...'
  LOADED-SUCCESS: '&8[&3Tr&bMenu&8] &bINFO &8| &7成功加载了 &a{0} &7个有效菜单... &8[&7{1} Ms&8]'
  LOADED-FAILURE: '&8[&3Tr&bMenu&8] &6WARN &8| &7共计有 &6{0} &7个菜单加载失败, 请检测诊断错误.'
  DEPEND-EXPANSIONS-REQUIRED: '&8[&3Tr&bMenu&8] &7目标菜单需要安装以下 PlaceholderAPI 变量才能使用, TrMenu 正在自动下载中... &6{0}'
  NOT-EXIST: '&8[&3Tr&bMenu&8] &7目标菜单不存在...'
  NOT-ENOUGH-ARGS: '&8[&3Tr&bMenu&8] &7此菜单要求你至少提供 &6{0} &7个有效参数.'
  FORCED-CLOSE:
    ==: TITLE
    title: '&c&l菜单强制关闭'
    subtitle: '&7&l正在重载菜单配置...'
  LOADING-ERRORS:
    NO-SHAPE: '&7菜单 &6{0} &7的模板形状无效, &2{1}'
    NO-BUTTONS: '&7菜单 &6{0} &7未配置按钮节点'
    YAML: '&7菜单 &6{0} &7的YAML格式配置出错! &c{1} &8{2}'
    CONFLICT-OPEN-COMMANDS: '&7菜单 &6{0} &7与菜单 &6{1} &7的自定义开启命令有冲突...'
    CONFLICT-OPEN-ITEMS: '&7菜单 &6{0} &7与菜单 &6{1} &7的绑定Lore物品打开有冲突...'
    ICON-NO-CONDITION: '&7菜单 &6{0} &7的按钮节点 &3{1} &7条件图标的条件为空...'
    ICON-LOAD-FAILED: '&7菜单 &6{0} &7的按钮节点 &3{1} &7加载失败. &3{2}&8{3}'

COMMANDS:
  NOT-PLAYER: '&8[&3Tr&bMenu&8] &c你必须是一名玩家...'
  NO-PLAYER: '&8[&3Tr&bMenu&8] &c目标玩家不存在或不在线...'
  OPENED-FOR: '&8[&3Tr&bMenu&8] &3已为目标玩家打开菜单...'
  LIST:
    - '&8--------------------------------------------------'
    - '&3Tr&bMenu &7- Menu List *&8(点击聊天内容即可打开)'
    - ''
  LIST-FORMAT:
    - '&8▫ &6{0}'
  HELP-PAGE:
    ==: JSON
    text:
      - '&8--------------------------------------------------'
      - '&3Tr&bMenu &7- Advanced Dynamic Menu &6*{0}'
      - ''
      - '&8▪ <&7/&3{1} List@list> &8— &7 列出所有菜单'
      - '&8▪ <&7/&3{1} Reload@reload> &8— &7 重新载入所有菜单'
      - '&8▪ <&7/&3{1} Open [Menu] [Id]@open> &8— &7 为自己或他人打开一个菜单'
      - '&8▪ <&7/&3{1} About@about> &8- &7 查看插件信息'
      - ''
      - '&8--------------------------------------------------'
    args:
      list:
        hover: |-
          &7点击这里快捷执行此命令.
        command: '/trmenu list'
      reload:
        hover: |-
          &7点击这里快捷执行此命令.
        command: '/trmenu reload'
      open:
        hover: |-
          &7点击这里建议该命令.
        suggest: '/trmenu open'
      about:
        hover: |-
          &7点击这里查看插件信息.
        suggest: '/trmenu about'
```
{% endcode %}



