# SafeConnect FAQ

## 卸载SafeConnect仍然能上网，原理是什么？
学校会检测你使用的操作系统，如果检测到是Windows或者Mac则要求安装SafeConnect，如果是Linux则直接放行。所以我们可以把操作系统伪装成Linux就可以被学校直接放行了。

## 怎样伪装成Linux操作系统？
修改浏览器的UserAgent

## SafeConnect如何检测你的操作系统？
浏览器在上网的时候，会告诉网站你的操作系统是什么。如果你上的那个网站不是加密的，SafeConnect就可以通过偷窥你跟网站的通讯，来判断你的操作系统。

## 为什么会不断出现“SafeConnect is detecting your device”页面？
SafeConnect在成功检测到你的操作系统以后，只会给你放行一小段时间。如果这段时间过了，他们还没有再次成功检测操作系统，那么他们就把你的网络连接给断开。

## 怎样让SafeConnect成功检测你的操作系统？
访问未加密网站

## 什么网站是加密的，什么网站是未加密的？
`http://` 开头的网站都是非加密的，`https://` 开头的网站都是加密的
也可以通过浏览器地址栏有没有一个锁的图标来判断，如果没有锁的图标，就是非加密的，如果有，就是加密的。比如说大型同性交友网站github.com就是加密的：

![GitHub address bar](github-address-bar.png)

而百度就是未加密的：

![Baidu address bar](baidu-address-bar.png)

## 如何避免被SafeConnect断网并出现“SafeConnect is detecting your device”页面？
两种方法。

第一种方法是：开一个没有加密的网页，然后设置每两秒自动刷新一下这个网页。

第二种方法是：写一个脚本程序，这个程序自动每隔一段时间就去访问一些非加密网站。