---
description: 100% 无损暴打 DM
---

# 迁移

## 支持菜单插件

* DeluxeMenus

## 如何迁移

* 一次性迁移多个菜单, 你只需将包含旧菜单插件的菜单文件的文件夹复制
* 丢进 **plugins/TrMenu**, 假设这个文件夹叫 **mFolder**
* 输入以下命令

```text
/TrMenu Migrate DeluxeMenus mFolder
```

* 如果一切顺利的话，你将能在 **plugins/TrMenu/migrated** 中找到迁移后的TrMenu格式菜单
* 旧的迁移过的菜单都会被加上后缀 **.MIGRATED** 标记

迁移后的新菜单都是TrMenu格式了，你可以直接放到 **plugins/TrMenu/menus** 中使用命令重载，即可使用

