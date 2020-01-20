---
description: 制作一个菜单，需要创建 YAML 文件
---

# 创建文件

## Method Ⅰ. 在菜单目录下创建

* 你只需进入目录 plugins/TrMenu/menus，创建以 .yml 结尾的 YAML 文件即可
* 文件名即为该菜单的唯一ID

{% hint style="info" %}
你可以在 menus 目录下创建子目录存放菜单文件，方便分类管理菜单
{% endhint %}

通过该方式创建的菜单，在服务器启动或执行命令 /TrMenu Reload 时候都会重新加载一遍

## Method Ⅱ. 自定义文件路径加载

需要在 settings.yml 中添加需要加载的文件路径

```yaml
# 自定义路径载入菜单
# (plugins/TrMenu/menus 目录及其子目录下的菜单默认均会加载)
MENU-FILES:
  - 'plugins/XXX/zzz.yml'
```

可以是绝对路径，实现多子服加载同一菜单

## Method Ⅲ. 配置文件内置菜单

你可以在 **settings.yml** 中创建你的菜单！

```yaml
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

