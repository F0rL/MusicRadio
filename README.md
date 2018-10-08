### [网页电台](https://f0rl.github.io/MusicRadio/)
#### 功能
提供了歌单选择、歌曲播放暂停下一曲、歌曲信息显示、背景图更改，能适配大尺寸显示变化。
#### 技术
- vh\vw实现设备屏幕适配
- @media实现响应式布局
- 使用jQuery对DOM对象进行操作
- 功能模块化代码
- 利用了自定义事件，使得歌单选择与歌曲播放解耦
- 事件代理
```
var EventCenter = {
  on: function(type, handler){
    $(document).on(type, handler)
  },
  fire: function(type, data){
    $(document).trigger(type, data)
  }
}
```
- 使用[Animate.css](https://daneden.github.io/animate.css/)+ jQuery自定义插件实现歌词的动画效果
通用模板
```
$.fn.boomText = function(type){
  type = type || 'rollIn'
  this.html(function(){
    var arr = $(this).text().split('').map(function(word){
      return '<span  style="opacity:0;display:inline-block">'+ word + '</span>'
    })
    return arr.join('')
  })

  var index = 0 
  var $boomTexts = $(this).find('span')
  var clock = setInterval(function(){
    $boomTexts.eq(index).addClass('animated ' + type) //注意animated后的空格
    index++
    if(index >= $boomTexts.length){
      clearInterval(clock)
    }
  }, 300)
}
```
#### 预览图
![](http://ww1.sinaimg.cn/large/90864b23gy1fw15qwakkvj218f0kxh01.jpg)