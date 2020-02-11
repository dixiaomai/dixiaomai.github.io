# 命令

## 主命令

* TrMenu
* Tmenu
* Menu

## Reload

> 手动重新载入菜单

* 参数：无
* 用法：/trmenu reload

## List

> 列出已经加载到内存的菜单

* 参数：无
* 用法：/trmenu list

## Open

> 为自己或指定玩家打开一个菜单

* 参数：\[菜单名\]  &lt;玩家名&gt;
* 用法：/trmenu open

## Item To Json

> 转写手持物品到 Json 文本, 以及逆向操作, Json 文本可在菜单中写入

* 参数：无 或 \[Json文本\]
* 用法：/trmenu item

## Run Action

> 为玩家执行 TrMenu 的动作
>
> 可以在其它插件调用，支持所有动作、参数！

* 参数：&lt;\#&gt;\[玩家\] \[动作\]
* 用法：/trmenu runAction
* 示例：
  * /trmenu runAction Arasple tell: Hello %player\_name%&lt;chance:0.5&gt;

{% hint style="info" %}
在玩家名前加修饰前缀 **\#** , 将会输出详细的动作属性，方便调试

如 /trmenu runAction \#Arasple xxxxx
{% endhint %}

## Template

> 在线模板轻松创建菜单，打开一个指定行数的容器，放入物品，关闭即可生成菜单！

* 参数：&lt;行数&gt;
* 用法：/trmenu template

## Share

> 粘贴你的菜单到 Hastebin，用于上报错误或分享菜单

* 参数：\[菜单名\]
* 用法：/trmenu share

## Migrate

> 导入菜单

{% page-ref page="../migrate.md" %}

## Sounds

> 打开一个极其方便的多页 GUI，可以预览所有音效（支持不同音调）
>
> 轻松复制音效名称，即可在 Sound 动作中使用

* 参数：\[过滤\]
* 用法：/trmenu sounds

{% page-ref page="../actions/advanced-actions/play-sound.md" %}

## Debug

> 别开

## Update

> 手动更新插件, 将下载最新的插件资源文件，当你下次重启服务器时便自动完成更新

* 参数: \[force\]
* 说明：
  * 执行 /trmenu update force 会强制下载最新构建, 忽略版本号差异
  * 可能升级一些小更新

## About

> TrMenu 的 Menu

