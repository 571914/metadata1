# metadata1

metadata1是登录亚马逊的时候，页面动态计算产生的一个字段，其内容经过加密混淆之后传回亚马逊并进行服务器端校验，从而阻止直接通过Http Post的方式绕过浏览器直接登录。

## metadata1包含了如下信息：
* 鼠标键盘交互信息  记录点击位置，点击次数，点击间隔，按键次数，按键间隔
* 页面加载的脚本的哈希信息  防止页面被篡改
* 浏览器的指纹  屏幕分辨率/插件/CSS/JS能力
* 电池信息  充电与否/充电时长
* 性能信息  页面加载的速度，各种时间基准
* 表单信息  记录email/password字段的点击位置，点击次数，点击间隔，按键次数，按键间隔

* CANVAS绘图/CRC校验/抽样

## 意义
通过复原metadata1，可以实现Http Post方式直接登录亚马逊，降低了自动化的难度，提高了执行效率；同时由于可以随意组合校验信息内的特征，一套方案即可模仿多种浏览器及软硬件环境。

## 接口
##### 参数
* email
* browserType [Chrome/Firefox/Edge/Internet Explorer]

##### 输出结果
ECdITeCs:4qz+eH24hr1pf+gx/vaqUcKtAqROfvGzo+...


![](https://github.com/571914/metadata1/blob/master/wechat.jpg)  
