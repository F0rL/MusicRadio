### [kuma的网页电台](https://f0rl.github.io/MusicRadio/)
#### 功能
提供了歌单选择、歌曲播放暂停下一曲、歌曲信息显示、背景图同步更改，能适配大尺寸显示变化。
#### 技术栈
- vh\vw实现设备屏幕适配
- @media实现响应式布局
- 使用jQuery对DOM对象进行操作
- 功能模块化代码
- 利用了自定义事件，使得歌单选择与歌曲播放解耦
- 事件代理
- 使用[Animate.css](https://daneden.github.io/animate.css/)+ jQuery自定义插件实现歌词的动画效果

#### 关键字
CSS3、 jQuery、响应式、操作DOM

#### 问题点
- 对于响应式界面,vh、vw要看情况选一个作为参照，不建议混用
- 字体图标库要考虑到统一性，外链引用选择合适的cdn加速
- 面向对象编程能够使代码更为简洁，也增加了代码的可读性
- 对于点击发生动画的事件，要增加一个验证状态，避免点击过快引起bug

#### 预览图
![](http://ww1.sinaimg.cn/large/90864b23gy1fw15qwakkvj218f0kxh01.jpg)