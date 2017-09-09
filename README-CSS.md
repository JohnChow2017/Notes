## NOTES-CSS

### 文本设置

#### 常见样式：<br>
>font-size<br>
font-family<br>
font-weight 文字着重<br>
font-style 文字倾斜 ltalic<br>

>line-height<br>
color( 英文\RGB\十六进制 )<br>

>text-align 文本对齐方式<br>
text-indent 首行缩进（em缩进字符）<br>
text-decoration 文本修饰 underline,line-through<br>

>letter-spacing 字母间距<br>
word-spacing 单词间距（以空格为解析单位）<br>

>font：font-style | font-weight | font-size/line-height | font-family 符合样式需依此顺序<br>


### 图片

```html
<img src='1.png' alt='如果无法显示图像，浏览器将显示替代文本' />
```

### a标签

功能：链接、下载、锚点（a锚点：添加id属性）
```html
<a href='www.baidu.com' target='_blank'>在新窗口中打开被链接文档。</a>
```
```html
<base target='_blank' />   //(在head中)将定义页面中所有连接的打开方式
```

### span标签
```html
<span>建议使用span标签区分样式</span>
```

### 列表
```html
<dl>      //定义列表
  <dt>定义列表标题</dt>
  <dd>定义列表项</dd>
</dl>
```

### 选择符
群组选择符：
```css
#box1,#box2{width:100px; height:100px; background:#red}
```


