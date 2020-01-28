# 高级商店

## 目标效果

> 实现三层 GUI, 即 `商店分类`、`分类下商品`、`商品出售/购买选择器` 
>
> 动态效果，逼格音效，TITLE/ACTIONBAR 等美观消息提醒
>
> Esc 返回上级菜单
>
> 数量选择器有范围限制, 如 0 - 64
>
> 100% 完全可自定义、二次修改

![](https://i.loli.net/2020/01/28/srxJRQwjFh52ALG.gif)

## 准备

TrMenu 1.15

PlaceholderAPI 2.10.4

Vault 1.7.1

EssentialsX 2.17.1.0 \(或任意与 Vault 挂钩的货币系统\)

**需下载的 PlaceholderAPI 变量拓展**

* CheckItem
* Math
* Vault

## 实现思路

创建两个独立的 出售/购买 \(数量选择器\) 处理菜单, 不必为每个商品创建独立的, 更方便灵活 利用参数 + 动态材质实现需购买/出售商品的信息传递 利用参数 + 计算变量实现商品数量的动态修改 利用计算变量实现商品价格的动态计算

## 配置

**\[!\]** 这仅是一个**模板**配置，**不可直接使用**，需要你**自行创建**更多的商品分类、商品等

如何获得配置

* 注册并验证邮箱，登录到 B.BBS [https://bbs.arasple.me/](https://bbs.arasple.me/)
* 配置分享即在 [https://bbs.arasple.me/d/5](https://bbs.arasple.me/d/5)

