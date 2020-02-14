---
description: 整理一些常见问题，持续更新
---

# 常见问题

{% hint style="info" %}
你可以在本页使用 **搜索** 功能，快速定位自己的问题
{% endhint %}

## TrMenu 是动态菜单，会不会爆卡炸掉我服务器？

* 会

## 我怎么绑定菜单到某物品上？

* TrMenu 支持绑定菜单到指定 Lore 上，会自动识别交互的物品
* **不支持** 仅绑定原版物品，对这项有需求的建议使用其它插件（物品执行命令等）

{% page-ref page="../menu/menu/setup.md" %}

## 为什么是洋文，怎么切换到中文

{% embed url="https://trmenu.trixey.cn/v/chinese/start/configure\#pei-zhi" caption="读你妈的 Wiki 去" %}

## 我怎么启用菜单参数功能啊？

* 怎么启用，你娘的认真读完 Wiki 了吗？

{% page-ref page="../menu/menu/setup.md" %}

## 我的配置提示 YAML 格式错误，明明对了的，怎么办？

* 对你个头，自己用工具看看你错在哪

{% embed url="http://www.bejson.com/validators/yaml/" %}

## 这个插件太难了，我放弃了

![n&#xED;n p&#xE8;i ma](../.gitbook/assets/npm.jpg)

## Shape 可真垃圾，我不想用

* 不用就不用，你单独设置 Rows / Size 就行了

## 为什么这司马 wiki 这么慢？

* 爪巴 梯子
* 下载离线版

## 我的布局 Shape 字符不够用怎么办？

* 字母（区分大小写），各种符号，实在不行汉字都可以

## 为什么我打不开菜单

* **有提示**
  * 提示没权限
    * 提示来自 TrMenu，则检查菜单的 Open-Requirement 项
    * 不知道提示来自哪，用 LuckPerms Verbose 过滤定位权限
  * 其它
    * 不知道
* **无提示**
  * 菜单是不是已加载、无报错
  * 用 LuckPerms Verbose 过滤定位权限
  * 别的玩家能打开
    * 不知道

## 玩家能随便刷出菜单的物品

* 物品是假的
  * 无解
* 物品是真的
  * Mod服
    * 第三方涉及容器的 Mod
  * 非 Mod 服
    * 无解

## 动态更新慢，即使周期设置非常低

* 开启菜单选项 

  ```text
  Options.Update-Inventory
  ```

## 为什么点按钮无效果

* 你的菜单动作格式错了，注意节点、缩进

## 怎么跨服

![n&#xED;n p&#xE8;i ma](../.gitbook/assets/npm.jpg)

## 怎么发公告消息

![n&#xED;n p&#xE8;i ma](../.gitbook/assets/npm.jpg)

## 能不能导入 BossShop \(Pro\)

* 目前不能，未来暂无相关计划

## 为什么不支持 CommandPrompter，那么好用

* ~~CommandPrompter 真菜，还占你 700kb~~
* TrMenu 自带更强、更灵活可拓展的输入捕获器

{% page-ref page="../actions/functional-actions/input-catcher.md" %}

## 聊天输入捕捉器怎么用？

* 如果你实在实在看不懂的话，就自己摸索吧
* 我也没办法

## 每日礼包一定要用 LuckPerms 吗

* 任何支持限时权限的插件都行

## 能做点卷商店吗？

* 什么类型的商店都可以做，只要提供余额相关的 PlaceholderAPI 变量
* 你可以参考几个示例，实现逻辑是一样的

## 我能不能

* 做交易菜单
* 做玩家仓库

答：**你不能**

