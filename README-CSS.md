## NOTES--HTML\CSS


### PS基础
* 前端需要的PS技能:<br>
标尺（快捷键：Ctrl R，主要是拖出参考线。矩形区域选择的时候，按住Ctrl，就能贴合参考线） <br>
盖印可见图层（Ctrl Alt Shift E）<br>
储存为web格式（Ctrl Alt Shift S）<br>

* 图片格式:<br> 
JPG：不支持透明半透明，所有空白区域填充白色（网页中的大图、高清图：体积大） <br>
GIF：支持透明，不支持半透明（网页中的小图标、动态图片） <br>
png8：支持透明，不支持半透明（网页中的小图标） <br>
png24：支持透明，也支持半透明（图像中存在半透明效果的图片）<br>

* PSD测量注意事项 - 文字右方和下方会有1像素的默认间隙

### 代码初识
html 超文本标记语言（结构）<br>
CSS 层叠样式表（样式）<br>
js javascript（行为）<br>
文件编码格式与代码编码格式一致的时候，网页才不会出现乱码，才可以显示正常。<br>

GB2312 中文简体标准<br>
utf-8 国际标准<br>

* border
solid dash dotted(IE6不支持)<br>

* padding
padding-top/right/bottom/left<br>
内边距相当于给一个盒子加了填充厚度，会影响盒子大小<br>

* margin
margin-top/right/bottom/left<br>
上下外边距会叠压<br>
父子级包含的时候，子级的margin top会传递给父级；（内边距替代外边距）<br>
如果给一个盒子仅设置margin-left: auto，那么盒子会跑到最右边；如果设置margin-right: auto，那么盒子就会跑到最左边。同时设置margin-left和margin-right为auto，可以使盒子居中。<br>

* 盒模型和结构样式
盒子大小 = border + padding + width/height<br>
盒子宽度 = 左border + 左padding + width + 右padding + 右border<br>
盒子高度 = 上border + 上padding + height + 下padding + 下border<br>

复合属性：一个属性多个属性值的命令<br>

* 常见文本设置
font: font-style	font-weight	font-size/line-height	font-family;<br>
font-size（一般为偶数，中文最小号12px）<br>
font-family（中文默认宋体、西文默认是arial，可用逗号分隔多种字体）<br>
color（英文、rgb、十六位进制色彩值）<br>
line-height（文字是在行高的上下居中）<br>
text-align<br>
text-indent（首行缩进，用em缩进字符）<br>
font-weight<br>
font-style<br>
text-decoration：underline、overline、line-through<br>
letter-spacing 字母间距<br>
word-spacing（以空格为解析单位）单词间距<br>

* img
注意写img的alt属性<br>
把img放到一个块里面，默认img与该块的下边框有几个像素的间距。为了解决这个问题，可以为img添加样式display: block;但是这种解决方法有局限性。<br>
另外一种方法是给图片添加vertical-align: top;也可以。<br>

* a标签
target=”_self”/”_blank”<br>
在head中添加如下代码，可以让页面中所有的链接都在新页面中打开，其中base代表默认<br>
<base target="_blank"/> <br>

a标签的作用:<br>
链接（a标签中放链接）<br>
下载（href的路径是文件路径）<br>
锚点（a的href中放的是id）<br>


* 常见标签和SEO浅析
标题h标签<br>
段落p标签<br>
强调strong标签（粗体）<br>
强调em标签（斜体）<br>
span标签<br>
有序列表ol标签<br>
无序列表ul标签<br>
列表项li<br>
定义列表dl<br>
定义列表标题dt<br>
定义列表项dd<br>
浅析SEO（搜索引擎优化）<br>

部分方法： 1. 页面标签语义化 2. 使用对SEO有利的标签：h1/h2/h3/strong/em… 3. 提高页面关键词密度 4. 其他<br>

SEM：搜索引擎营销；（包含SEO）<br>

* 基础选择符
id选择符 #<br>
class选择符 .<br>
类型选择符 p div a img等<br>
群组选择符 用逗号,分隔<br>
包含选择符 用空格分隔<br>
通配符 *<br>

* 选择符优先级
同级样式默认后者覆盖前者<br>
样式优先级<br>
类型选择符（1）<br>
class选择符（10）<br>
id选择符（100）<br>
style行间样式（1000）<br>
js动态修改行间样式<br>

* a伪类
link 未访问（默认）<br>
hover 鼠标悬停（鼠标划过）<br>
active 链接激活（鼠标按下）<br>
visited 访问过后（点击过后）<br>
注意书写顺序 a:link → a:visited → a:hover → a:active，--(love-hate)<br>
这样在链接点击之后，a:hover和a:active的样式才不会被a:visited的样式覆盖，仍然起效。<br>

a伪类的应用：<br>

四个伪类全用（搜索引擎、新闻门户、小说网站）<br>
一般网站只用 a {} 和 a:hover {}<br>

a伪类的兼容:<br>
IE6不支持a以外其他任何标签的伪类<br>
IE6以上的浏览器支持标签的hover伪类<br>

* 标签默认值样式重置
```html
/* 默认样式重置（css reset） */
body, div, p, h1, h2, h3, h4, h5, h6, dl, dd { margin: 0; font-size: 12px; /* font-family */ }
ol, ul { list-style: none; padding: 0; margin: 0; }
a { text-decoration: none; }
img { border: none; }
```
<br>

* 标签基本特性和转换:
1.内联、内嵌、行内属性标签： a、span、strong、em、img、input、select、textarea<br>
默认同行可以继续跟同类型标签<br>
内容撑开宽度<br>
不支持宽高<br>
不支持上下的margin和padding<br>
代码换行被解析（如果内联元素在代码中换行了，那么在页面中，就会体现为内联元素之间的空隙）<br>

2.块标签 p、div、h1~h6、ol、ul、dl、form<br>
默认独占一行显示<br>
没有宽度时，默认撑满一排<br>
支持所有css命令<br><br>

display: block; 显示为块<br>
display: inline; 显示为内嵌<br>

* inline-block的特性和应用
特性：<br>

块在一行显示<br>
行内属性标签支持宽高<br>
没有宽度的时候，内容撑开宽度<br>
问题：<br>

代码换行被解析（代码中inline-block换行写，在页面中inline-block元素之间会有空隙）<br>
IE6/7不支持块属性标签的inline-block<br>

关于代码换行解析（页面中内联元素和inline-block元素之间的空隙）：<br>
空隙为一个空格的大小，也就是页面上默认字号的一半。比如页面上默认字号为12px，那么它们之间的空隙就是6px。<br>

inline-block的应用：分页导航<br>

分析结构（div包一排a）
a标签不支持宽高 并在一排显示，因此要设置inline-block<br>
有hover效果<br>
当前页的页码上不能点<br>
cursor指针样式（规定要显示的光标的类型）<br>
cursor: pointer	text	move …<br>
cursor: url(hand.cur), pointer; 如果前面图片没引入进来，就用后面的pointer<br>

* 前端规范
标签闭合<br>
html标签可用tab键缩进<br>
属性值带引号<br>

<!– html注释 –> 注意注释内容与横线之间要有空格<br>
/* css注释 */ 注意星号与文字之间要有空格<br>
ul, li/ ol, li/ dl, dt, dd拥有父子级关系的标签<br>
p, dt, h标签，里面不能嵌套块属性标签<br>
a标签不能嵌套a<br>
尽量不要用内联元素去嵌套块（例如：p标签中添加了h或者div块标签，一个p标签会被隔成两个。注意，这里指的是块标签。如果p里面放了span，然后把span的样式设置了display: block;，p标签不会被隔成两个。）<br>

* 浮动的原理 left/right/none 以及清除浮动的各种方法:

-浮动的定义<br>

元素加了浮动，会脱离文档流，按照指定的一个方向移动，直到碰到父级的边界或者另外一个浮动元素停止。<br>

1.使块元素在一行显示<br>
2.使内嵌元素支持宽高<br>
3.在不设置宽度的时候宽度由内容撑开<br>
4.脱离文档流（文档流是文档中可显示对象在排列时所占用的位置）<br>
5.提升层级半层（只够挤进元素本身，元素里面的内容，如文字，图片等，还是会被挤出来）<br>
clear left/right/both/none<br>

clear控制元素的某个方向上不能有浮动元素<br>

* 清除浮动（撑开父级元素）
方法一、 给父级元素加高（问题：扩展性不好）<br>

方法二、 给父级也加浮动（问题：页面中所有元素都加浮动，margin左右自动失效。）<br>

方法三、 用父级添加display: inline-block来清除浮动（问题：margin左右自动失效）<br>

方法四、 在浮动元素下边加上<div class=”clear”></div>空标签清浮动（问题：IE6最小高度19px；解决后IE6下还有2px偏差）<br>
<br>
```css
.clear {
    height: 0px;
    clear: both;
    font-size: 0;
}
```
<br>
-- IE6下的最小高度问题：
在IE6下高度小于19px的元素，高度会被当作19px处理<br>

解决办法一：给该元素加font-size: 0; 这样只能处理到最小2px，再小也没办法了。<br>

解决方法二：为该元素添加overflow: hidden;样式 ——这也是处理IE6下最小高度的最常用方法。<br>

方法五、在浮动元素下面加<br clear=”all” /> （问题：不符合W3C标准，样式混入了html）<br>
方法六、给浮动元素的父级元素加上clear类，然后给该元素的after伪类设置如下样式（问题：IE6、7不支持after伪类，为了兼容IE6、7，还要给父级元素加上样式zoom:1）<br>
<br>
```css
.clear:after {
    content: "";
    display: block;
    clear: both;
}
```
<br>
注意：在IE6、7下，浮动元素的父级有宽度的话，就不用清除浮动。<br>

在IE中，子元素的宽高要么是跟着父级走的，要么是跟着内容走的。这个可以用haslayout来调节。但是haslayout不会自动控制。haslayout的默认值为false。但是用了特定样式的时候，haslayout会变成true。具体可以看百度百科的词条。<br>

当haslayout触发的时候，会根据元素内容大小或者父级的大小来重新计算元素的宽高。所以在IE6、7下，如果给浮动元素的父级加了宽高的话，那么触发了haslayout。该父级元素就根据其内容，及子元素来重新计算宽高，也就清除了浮动。如果父级元素没有加宽高的话，通过加zoom: 1;来触发haslayout，就可以解决问题了。也就是说，为了兼容IE6、7，除了给父级元素加上clear类，然后该给父级元素的after伪类添加上述样式之外，还要给该父级元素加上zoom: 1;的样式。也就是如下代码：<br>

`最终推荐使用的清楚浮动的方法:`

<br>

```css
.clear { /*用来处理IE6、7*/
    zoom: 1;
}
.clear:after { /*用来处理其他浏览器*/
    content: "";
    display: block; /*或display: table;也可以*/
    clear: both;
}
```
<br>
zoom的作用就是放大或缩小。zoom在不同浏览器中不兼容。<br>

overflow的作用：<br>

overflow并不是各浏览器兼容的。效果不同。overflow针对溢出的。<br>

overflow的各个设置：<br>

auto 溢出显示滚动条<br>
scroll 默认就显示滚动条<br>
hidden 溢出隐藏<br>
visible 默认值<br>
<br>
要执行overflow样式，首先要检测父级元素中的内容是否超出其宽高。如果子元素是浮动元素，父级元素又设置了固定宽高的话，如果子元素大于固定宽高的父级元素，并且父级元素设置了overflow: auto;会看到有滚动条出现。那说明，overflow不仅可以检测到浮动元素是否溢出，而且也可以让父级元素包住浮动的子元素。那么，即使父级元素没有设置宽高，给父级元素设置了overflow的样式，也可以清除浮动。<br>
<br>
方法七：给浮动元素父级加overflow: hidden;或overflow: auto;来清除浮动，并且一定要配合zoom: 1使用。（问题：IE6下，overflow没有包住浮动子元素的功能，为了兼容，还是要加zoom: 1来解决一下）。<br>
方法八：给浮动元素的父级元素添加position: absolute或者position: fixed，都可以清除浮动。<br>

* 浮动的问题
1.推荐在IE6、7下，元素浮动要并在同一行的元素都要加浮动(例如，第一个box浮动，第二个div里面的文字会排到第一个box的同行后面，但是在IE6下，第二个元素中的文字与第一个float的box有3px的间距。但是在正常情况下，两者之间是不应该有间距的。)<br>
<br>
##### 兼容性问题

IE6双边距bug（IE6下块属性标签浮动，并且有横向margin，横向margin加倍。）<br>
IE6<br>
浮动<br>
横向margin<br>
块属性标签（解决方法：加display: inline;)<br>
IE6下li部分兼容性问题：<br>
左右两列布局，右边右浮动IE6、7下折行；（解决方法：不仅右侧元素向右浮动；左边元素也要添加向左浮动）<br>
IE6、7 li中的元素都浮动。在IE6、7下li元素下方会产生4px间隙问题；（在IE6、7下li本身没有浮动，但是其中的内容浮动了，li下就会多出来几个px的间隙）<br>
（解决方法1： 给li也加浮动。注意给ul清除浮动。<br>
  解决方法2：不给li加浮动，但是给li加vertical-align: top/middle;都可以）<br>
<br>
* vertical-align的作用
作用一：vertical-align是垂直对齐样式。要给每个要对齐的元素都加上这个属性。vertical-align对于浮动的元素是失效的，浮动元素是默认顶部对齐的。<br>
作用二：用于清理图片下方的空隙。（将img放在块中，img下方会有几个像素的空隙。可以为img设置display: block;来清理，但是这种方法有局限性，因此推荐给img添加vertical-align: top;样式来清理。）<br>

#### 定位
<br>
* 相对定位
添加了position: relative;的元素就变成了定位元素，具有以下特性：<br>
<br>
不影响元素本身的特性<br>
不使元素脱离文档流<br>
如果没有定位偏移量，对元素本身没有任何影响<br>
定位元素位置控制<br>
<br>
top/right/bottom/left 定位元素偏移量<br>
<br>
* 绝对定位
使元素完全脱离文档流<br>
使内嵌支持宽高<br>
块属性标签内容撑开宽度<br>
如果有定位父级相对于定位父级（而不是结构父级）发生偏移，没有定位父级相对于整个文档（不是body）发生偏移（body、html和文档之间的关系是body之上有html，html之上有文档）<br>
相对定位一般都是配合绝对定位元素使用<br>
z-index: [number]; 定位层级<br>
<br>
定位元素默认后者层级高于前者（不论是相对定位还是绝对定位）<br>
<br>
* 滤镜和遮罩弹窗<br>

```html
<div class="mask"></div> //遮罩
<div class="alert"></div> //弹窗
```

<br>

```css
body, html { //这里是为了兼容IE6。如果不给body和html加height: 100%的话，IE6下的蒙板只在最上面显示一条）
  height: 100%;
}
.mask { //遮罩的样式
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #000;
  opacity: 0.5;
  filter:alpha(opacity=50);
}
.alert { //弹窗的样式
  width: 400px;
  height: 200px;
  background: #fff;
  border: 2px solid black;
  position: absolute;
  top: 50%;
  left: 50%;
  margin-top: -102px; //注意盒子的高度是200像素加上边框宽度×2，也就是204px
  margin-left: -202px; //注意盒子的高度是404，而不是400.所以一般就是202px。此处一定要注意。
}
```

* 固定定位
position: fixed 固定定位：与绝对定位的特性基本一致，差别是始终相对整个文档进行定位；<br>
<br>
问题：IE6不支持固定定位<br>
<br>
* 滤镜
标准浏览器下：不透明度：opacity: 0~1; 0是完全透明；1是完全不透明。<br>
IE私有滤镜：filter:alpha(opacity=0~100); 0是完全透明，100是完全不透明。(IE Tester是不支持IE的filter滤镜的)<br>
<br>
* 定位其他
position: relative	absolute	fixed	static	inherit;<br>
position: static; //默认值<br>
position: inherit; //从父元素继承定位属性的值<br>
<br>
* 定位的一些问题
1.相对定位的一些问题<br>
<br>
在IE6下，父级的overflow: hidden; 是包不住子集的相对定位的。例如：<br>
<br>

```css
#box1 {width: 500px; height: 300px; background: blue; overflow: hidden;}
#box2 {width: 300px; height: 500px; background: yellow; position: relative;}
```

这两个盒子，子元素box2比父元素box1要长，虽然父级添加了overflow: hidden; 但是一旦子元素添加了position: relative; 在IE6下，子元素还是会撑破父元素。<br>
<br>
解决方法，在父级也加一个相对或绝对定位position: relative/absolute; 就可以包住子元素了。<br>
<br>
绝对定位的一些问题<br>
<br>
IE6下，定位元素的父级的宽高是奇数的话，那么该定位元素的right和bottom都有1像素的偏差。例如：<br>

```css
#box1 {width: 300px; height: 300px; border: 1px solid black; position: relative;}
#box2 {width: 50px; height: 50px; backgruond: #7c1; position: absolute; right: -1px; bottom: -1px;} 
```

其中box2是box1的子元素。请仔细观察。当box1的宽高为300px的时候，box2会遮掉box1右下角的边框，这是正常的。但是当box1的宽高是301、303等奇数时，在IE6下，box2没有遮掉box1右下角的边框，这正是因为出现了1px的偏差。这个问题，没有好办法规避。<br>
<br>
position: absolute; 绝对定位的元素子级的浮动可以不用写清浮动方法<br>
<br>
2.固定定位的一些问题<br>
<br>
position: fixed; 固定定位元素子级的浮动可以不用写清浮动方法；（IE6不兼容）<br>
<br>
* 表格标签特性与默认样式重置
一个完整的表格结构：

```html
table
    thead
        tr
            th …
tbody
    tr
        td …
tr
    td …
tfoot
    tr
        td …
```

* table的默认样式重置
```css
th, td { padding: 0; }
table {border-collapse: collapse; }
/* table css reset */
```

注意事项：<br>
<br>
1.不要给table, th, td以外的表格标签加样式<br>
2.单元格默认平分table的宽度<br>
3.th里面的内容默认加粗，并且左右上下居中显示<br>
4.td里面的内容默认上下居中，左右居左显示<br>
5.table的宽度决定整个表格的宽度<br>
6.table里面的单元格宽度会被转换成百分比<br>
7.建议表格里面的每一列都必须有宽度（防止单元格内容变更，使整个表格布局改变）<br>
8.表格中同一竖列继承最大宽度<br>
9.表格中同行继承最大高度<br>
10.table的标签基本特性就是display: table，既不是块也不是内嵌。<br>
<br>
单元格合并<br>
<br>
colspan：属性规定单元格可横跨的列数<br>
rowspan：属性规定单元格可竖跨的行数<br>
<br>
* 表单元素和样式重置
表单元素大多是inline-block<br>
<br>
form 表单<br>
<input type=”…” name=”” value=”” /><br>
text 文本框<br>
password 密码<br>
radio 单选（为多个选项添加同一个name，实现单选）<br>
checkbox 复选（checked：默认选中；disabled：禁用）<br>
submit 提交<br>
reset 重置<br>
button 按钮<br>
image 图片（基本不太用）<br>
file 上传（不同浏览器没法兼容）<br>
hidden 隐藏<br>
select标签配合option使用 下拉选框（默认显示第一项，也可以用selected指定默认选项）<br>
textarea 文本域<br>
label的用法（用for进行关联）：<br>

```html
<input type="radio" name="gender" id="a" /><label for="a">男</label>
<input type="radio" name="gender" id="b" /><label for="b">女</label>
```

默认样式重置<br>

```css
form {margin: 0;} //IE下form是有外边距的
input {margin: 0; padding:0;}
select {margin: 0;}
textarea {margin: 0; padding: 0; resize: none; overflow: auto;}
```

select元素支持宽度、高度支持并不完善。单选框、复选框对宽高的支持不完善<br>
<br>
可以用outline: none去掉表单元素的焦点线。<br>
<br>
* 表单元素的问题
表单元素兼容性问题<br>
<br>
IE6下input背景滚动：<br>
<br>
文本框：当内容比框宽的时候，该文本框背景会被挤跑。解决方法：将该文本框用一个div包起来。在这个div上设置背景图片。然后把该文本框的宽高设置为与div相同；把文本框的边框去掉，文本框的背景设置为无。<br>

```html
<div class="box">
    <input type="text name="" class="text" />
</div>
/* input {margin: 0; padding: 0;}
.text {width: 300px; height: 40px; border: 1px solid blue; background: url(sun.jpg) 0 center no-repeat #ffc;}
*/
 ```
 
//以上这种仅针对input的样式设置，在IE6下，当输入的内容宽于文本框时，背景会跑掉。
```css
.box {width: 300px; margin-top: 50px; height: 40px; border: 1px solid blue; background: url(sun.jpg) 0 center no-repeat #ffc;}
.box input {width: 300px; height: 40px; border: none;}
```
//以上这种设置方式，其实是把样式加到div上，然后让文本框变成透明，并且与外面的div同样大小，从而变成同样的视觉效果。<br>
<br>
outline轮廓线：<br>
<br>
a标签轮廓线去除方法：<br>

```html
<a href=”#” onfocus=”this.blur();”>…</a>
<a href=”#” hidefocus>…</a>
```

<br>
##### HTML和CSS进阶
滑动门技术<br>
<br>
滑动门的概念<br>
<br>
滑动门并不是一项全新的技术。它是利用背景图像的可层叠性，并允许他们在彼此之上进行滑动，以创造一些特殊的效果。<br>
<br>
左上和又上是圆角的按钮实现方式（按钮宽度可以随意变动）：<br>

```html
<div class="btn">
    <div class="btnL">
        <div class="btnR">妙味课堂</div>
    </div>
</div>
```

<br>

```css
.btn {width: 100px; background: url(img/btn.png) repeat-x;) //btn.png为中间的一像素平铺
.btnL {background: url(img/btnL.png) no-repeat;} //btnL.png是带左角的那一部分
.btnR {height: 31px; background: url(img/btnR.png) no-repeat right 0;} //btnR.png是带右角的那一部分
```

以上方法比较麻烦；优化方法为（按钮宽度可以变动，但是不能宽于btn2.png的宽度）：<br>
<br>

```html
<div class="btn">
    <div class="btnR"></div>
</div>
```

<br>

```css
.btn {width: 100px; background: url(img/btn2.png) no-repeat;} //btn2.png是左角部分外加中间部分
.btnR {height: 31px; background: url(img/btnR.png) no-repeat right 0;} //btnR.png是右角的那一部分
```

但是第二种方法没有第一种方法的扩展性好。第二种方法受到btn2.png这张图片宽度的限制。因此，对于扩展要求高、图片比较大的，尽量使用三层嵌套的方法。对扩展要求不高、图片比较小的，用两层嵌套。<br>
<br>
元素的宽度由内容撑开：<br>

```css
display: inline;
display: inline-block;
float
position: absolute;
position: fixed
```

宽高可扩展的圆角的实现方式<br>
<br>
简单的方法：使用CSS3里面的border-radius<br>
<br>
利用滑动门的三层嵌套方法：<br>

```html
<div class="box>
    <div class="boxHead">
        <div class="boxHeadL">
            <div class="boxHeadR"></div>
        </div>
    </div>
    <div class="boxC">
        圆角框中的内容
    </div>
    <div class="boxFoot">
        <div class="boxFootL">
            <div class="boxFootR"></div>
        </div>
    </div>
</div>
```

<br>

```css
.box {width: 200px; margin: 30px auto;}
.boxHead {background: url(boxH.png) repeat-x; height: 9px; overflow: hidden;}
.boxHeadL {background: url(boxHL.png) no-repeat;}
.boxHeadR {background: url(boxHR.png) no-repeat; right 0; height: 9px;}
.boxFoot {background: url(boxF.png) repeat-x; height: 9px; overflow: hidden;}
.boxFootL {background: url(boxFL.png) no-repeat;}
.boxFootR {background: url(boxFR.png) no-repeat right 0; height: 9px;}
.boxC {border-left: 1px solid #e5e5e5; border-right: 1px solid #e5e5e5;}
```

背景透明的圆角框实现<br>
<br>
首先在切图的时候，圆角的部分，就要切背景透明<br>

```html
<div class="btn">
    <div class="btnL">
        <div class="btnR"></div>
    </div>
</div>
```

<br>

```css
.btn {width: 100px; margin: 0 auto; background: url(btn.gif) repeat-x;}
.btnL {background: url(btnL.gif) no-repeat; position: relative; left: -9px;}
.btnR {background: url(btnR.gif) no-repeat right 0; height: 25px; position: relative; right: -18px;} 
```

<br>
//注意，因为btnL设置了left: -9px; 导致btnR也向左移了9px，要让btnR比btn还要向右移除9px，就要设置一个相对右移的9*2=18像素才行<br>
以上的写法有些麻烦，更为简便的方法是：<br>

```html
<div class="btnL">
    <div class="btnR">
        <div class="btn"></div>
    </div>
</div>
<!-- 注意这种写法与上面的那种方法，标签嵌套的顺序变了 -->
```

<br>

```css
.btnL {width: 100px; margin: 0 auto; background: url(btnL.gif) no-repeat;}
.btnR {background: url(btnR.gif) no-repeat right 0;}
.btn {height: 25px; background: url(btn.gif) repeat-x; margin: 0 9px;}
//这种方法是通过控制中间平铺的btn的宽度，使两边的圆角透出来的。
```
<br>

* CSS精灵
利用backgroudn-poition的设置，将小图拼成一个大图，从而减少HTTP请求。<br>
<br>
CSS sprites的优缺点：<br>
<br>
css精灵的优点：<br>
利用css精灵能很好地减少网页的http请求次数，从而大大提高页面性能。<br>
减少图片大小<br>
<br>
CSs精灵的缺点<br>
降低开发效率<br>
维护难度加大<br>

#### 兼容性
常见问题：<br>
<br>
一、IE6中，内容的宽高会撑开父元素设置的宽高。因此计算一定要精确，不要让内容的宽高超出父元素设置的宽高。<br>
<br>
二、IE6（7？）下元素浮动，如果宽度需要内容撑开就给里边的块元素都加浮动。<br>
<br>
三、在IE6、7下，元素要通过浮动并在一行，就给这行元素都加浮动。（如果第一个用浮动，第二个用margin-left，那么在IE6、7下，这两个元素之间会出现3像素的间隙，这也就是所说的3像素的bug）<br>
<br>
四、注意标签嵌套规范，例如不要在p标签里面嵌套块标签。<br>
<br>
五、IE6下的最小高度问题。IE6下元素的高度小于19px时，会被当作19px处理。解决方法：font-size: 0; 或者overflow: hidden; 推荐后面的方法。<br>
<br>
六、border的边框是1px dotted的点线的时候，在IE6下不支持。解决办法：切背景平铺。<br>
<br>
七：在IE6下，要解决margin传递，一定要触发haslayout。解决办法：添加zoom: 1;<br>
<br>
八，在IE6下，父级有边框的时候，子元素的margin值消失了。解决办法：触发父级的haslayout，也就是添加zoom: 1;<br>

（尽量在IE6下触发元素的haslayout，也就是添加zoom: 1; 可以避免掉很多兼容性问题。<br>
<br>
九：IE6、7只支持a标签的四个伪类，其他的伪类不支持<br>
<br>
十：在IE6、7下，inline-block是不支持块标签的。没有解决办法<br>
<br>
十一：IE6下的双边距bug。在IE6下，块元素有浮动和横向的margin值，横向的margin值会被放大成两倍。当设置的是`margin-right`的时候，是一行右侧第一个有双边距；当设置的是`margin-left`的时候，是一行左侧第一个元素有双边距，如果左右margin都设置了，那么一行的右侧第一个和左侧第一个都有双边距bug。解决办法：转成内嵌：`display: inline;`<br>
<br>
十二：在IE6、7下，li本身没浮动，但是li其中的内容有浮动，那么li下面就会产生一个间隙。解决办法：第一种解决办法：给li添加浮动（有时为了效果，还需要为li设置宽度）；办法二：给li添加垂直对齐方式：`vertical-align: top;`。注意：当IE6、7下最小高度问题和li间隙问题同时出现的时候，给li加浮动。因为如果用`overflow: hidden`解决最小高度，同时用`vertical-align: top`解决间隙问题，会发现li下面仍有间隙。因此碰到这种情况，要用给li添加浮动的方法来解决。<br>

十三：IE6下，当一行子元素占有的宽度之和与父级的宽度相差超过3像素，或者有不满行状态的时候，最后一行子元素的下margin在IE6下失效。没发现有解决办法。<br>
<br>
十四：IE6下的文字溢出bug。子元素的宽度和父级的宽度相差小于3像素时，并且两个浮动元素中间有注释或者内嵌元素，就会出现文字溢出bug。解决办法：把中间的注释和内嵌元素用div抱起来；或者把父级元素调大一些也可以。<br>
<br>
十五：在IE6下，当浮动元素和绝对定位元素是并列关系的时候，绝对定位元素会消失。解决办法：给绝对元素外面包个div。<br>
<br>
十六：在IE6、7下，子元素有相对定位的话，父级的overflow就包不住子元素了。解决办法：给父级也添加相对定位。<br>
<br>
十七：在IE6下，绝对定位元素的父级宽高是奇数的时候，元素的rigt值和bottom值会有1px的偏差。<br>
<br>
十八：IE6不支持固定定位。要用JS解决<br>
<br>
十九：opacity透明度只有标准浏览器支持，在IE6、7、8要通过滤镜filter来解决。<br>
<br>
二十：如果tbody和其中包含的tr都有背景的话，tbody的背景就会消失；如果thead和其中的tr都有背景的话，thead的背景也会消失。因此不要给这两个同时加背景。<br>
<br>
二十一：在IE6、7下，输入类型的表单控件上下各有1px的间隙。解决方法：给input添加浮动。<br>
<br>
二十二：在IE6、7下，输入类型表单控件加border: none;无效。解决办法：border: 0; 或者给input重置下背景。<br>
<br>
二十三：在IE6、7下，输入类型表单控件输入文字的时候，背景图片会跟着一块儿移动。解决办法：方法一：给背景图片添加fixed属性，但是这种方法在IE7下，背景图片有些错位。方法二：把背景图片加给父级，然后把input自己的背景设置为background: none;<br>
<br>
二十四：png问题。IE6不支持png透明背景的图片。解决办法：引入js文件DD_belatedPNG<br>
<br>
* 条件注释语句
下面这一段条件注释代码，IE6-9都可以解析出其中的内容，IE10以及其他标准浏览器则作为注释处理，不会在页面上显示。<br>
```html
<!--[if IE]>
这是IE
<![end if]-->
```
条件注释语句还有以下几种写法：<br>

```html
<!--[if IE 9]>
这是IE9
<![end if]-->
<!--[if IE 8]>
这是IE8
<![end if]-->
<!--[if IE 7]>
这是IE7
<![end if]-->
<!--[if IE 6]>
这是IE7
<![end if]-->
```
css hack<br>
<br>
针对不同的浏览器写不同的css样式的过程，就叫css hack！
<br>
远离CSS hack，有益身心健康！<br>
<br>
\9 IE10之前的IE浏览器解析<br>
<br>
星号*和加号+是IE7以及之前的IE浏览器解析<br>
<br>

_ 下划线是IE6以及IE6之前的IE浏览器解析<br>
<br>
针对chrome的css hack：@media screen and (-webkit-min-device-pixel-ratio: 0) {}<br>
<br>
用css hack解决IE6的png问题（原生的CSS办法，没法设置背景图片大小，也没法平铺）：<br>

```css
.box {width: 400px; height: 400px; background:url(img/png.png); _background: none; _filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(src="img/png.png", sizingMethod="crop");
```

样式优先级、提升样式优先级<br>

默认 < 类型 < class< id < style (行间) < js<br>
!important提升样式优先级权重<br>
在IE6下，在important后面加一条同样的样式，会破坏掉important的提升优先级作用，会按照默认的优先级顺序来走。<br>

#### 两种特殊布局

圣杯布局（双飞翼布局）<br>
<br>
左右宽度固定，中间宽度自适应伸缩，并且中间先加载<br>

```html
<div class="center"></div>
<div class="left"></div>
<div class="right"></div>
```

<br>

```css
body {margin: 0}
.center {height: 600px; background: #f60; margin: 0 200px;}
.left {width: 200px; background: #fc0; height: 600px; position: absolute; left: 0; top: 0}
.right {width: 200px; background: #fcc; height: 600px;position: absolute; left: 0; top: 0}
```

等高布局<br>
```html
<div class="wrap">
    <div class="left"></div>
    <div class="right"></div>
</div>
```

<br>

```css
body {margin: 0}
.wrap {width: 900px; margin: 0 auto; overflow: hidden;}
.left {width: 200px; background: red; float: left; padding-bottom: 10000px; margin-bottom: -10000px;}
.right {width: 700px; background: blue; float: right; padding-bottom: 10000px; margin-bottom: -10000px;}
```

IE6下使用margin负值的为题<br>
<br>
在IE6下使用margin负值，超出边界的部分会被截掉。解决方法是为这些元素添加相对定位即可。<br>
<br>
<br>
* 其他零散知识
热区<br>
```html
<img src="bigptr.jpg" usemap = "#Map" />
<map name = "Map">
    <area shape = "circle" coords = "378, 132, 56" href = "http://www.baidu.com">
    <area shape = "rect" coords = 462, 157, 566, 217" href = "http://www.google.com">
    <area shape = "poly" coords = "227, 251, 186, 220, 168, 221 ..." href = "http://www.qq.com">
</map>
```
map 热区<br>
area 点击区域<br>
shape = “circle” 圆形 rect<br>
coords = “圆心点x, 圆心点y, 原的半径”<br>
href 跳转地址<br>
shape = “rect” 矩形<br>
coords = “矩形左上角x, 矩形左上角y, 矩形右下角x, 矩形右下角y”<br>
shape = “poly” 不规则多边形<br>
coords = “第一个点x, 第一个点y, 第二个点x, 第二个点y,…… “<br>

* data uri
把图片src里面的地址用data uri代替<br>
<br>
优点：减少HTTP请求数<br>
缺点：无法被重复利用；会使文件变大<br>
在线工具: http://dancewithnet.com/lab/2009/data-uri-mhtml/create/1376100722.php<br>

* iframe
iframe外联框架。现在已经不太用了。<br>
```html
<iframe src="http://www.baidu.com" width="1200" height="600" frameborder = "0" scrolling="no"></iframe>
```
* flash引入
```html
<embed src=”1.swf width=”400” height=”400”></embed> embed标签就好用object标签包起来
<object>
    <embed src="1.swf" width="400" height="400"></embed>
</object>
```
flash透明<br>
```html
<param name=”wmode” value=”transparent”> wmode=”transparent”:
<object>
    <param name="wmode" value="transparent">
    <embed src="1.swf" width="400" height="400" wmode="transparent"></embed>
</object>
```
* 引入视频
在HTML5中：<br>
<br>
<video></video><br>
如果要兼容IE的话，要用flash来做。常用的两种方法：<br>
<br>
用Dreamweaver自带的视频播放器（只支持flv格式）<br>
借助其他视频网站（优酷等），通过复制网站声称的代码，实现嵌入视频。<br>
<br>
* 词内断行和省略号
text-overflow (clip ellipsis)<br>
white-space: nowrap<br>
word-break: break-all和word-wrap: break-word;<br>
文字溢出显示省略号，有三个样式设置缺一不可：<br>
一，给元素添加宽度width。<br>
二、设置overflow: hidden。<br>
三、white-space: nowrap。<br>
三个条件齐备之后，设置text-overflow: ellipsis才会其效果。给元素添加宽度是为了兼容IE6.在标准浏览器下，不给元素添加宽度，也可以。<br>
<br>
#### 盒模型的怪异模式
<br>
box-sizing 盒模型解析模式<br>
content-box 标准盒模型 width/height = border + padding + content<br>
border-box 怪异盒模型 width/height = content<br>
可视宽高<br>
<br>
可视宽： 元素的内蓉宽+padding+border<br>
元素的内容宽：元素里可以放内容的宽度<br>
怪异模式/怪异盒模型解析<br>
<br>
文档声明没有写或者写错，在IE6、7、8的盒模型解析就会进入怪异模式。<br>
<br>
可视宽：设置宽度<br>
内容宽：设置宽度-padding-border<br>
（可视高和元素的内容高同理。）<br>
<br>
* 隐藏元素
两种方法：<br>
<br>
display: none; 元素原文档位置不保留<br>
visibility: hidden; 元素的原文档位置会保留<br>
<br>
* 模拟固定定位
IE6不支持固定定位。那么在IE下用绝对定位模拟固定定位的第一种方法如下：<br>
```html
<div class="box">
    <div class="div"></div>
</div>
```

<br>

```css
html {height: 100%; overflow: hidden;}
body {margin: 0; height: 100%; overflow: auto;}
.box {height: 2000px;}
.div {width: 100px; height: 100px; background: red; position: absolute; left: 100px; top: 100px;}
```

上述代码中，绝对定位的.div是根据html的父级也就是document来定位的。原本滚动条是在document上的。但是html设置了`overflow: hidden;`，因此就把document上的滚动条hidden掉了；然后在body上加了`overflow: auto; `滚动条跑到了body身上。因此滚动滚动条的时候，滚动的是body，document的位置不变，因此依据document进行绝对定位的`.div`看起来就好像是固定定位的效果。<br>
<br>
以上方法也是存在问题的。<br>
<br>
模拟固定定位的第二种方法：<br>
```html
<div class="box">
    <div class="div"></div>
</div>
```

<br>

```css
.box {height: 2000px;}
.div {width: 100px; height: 100px; background: red; position: fixed; left: 100px; top: 100px; _position: absolute; _top: expression(eval(document.documentElement.scrollTop+100));}
```

<br>

* 未知宽高的img如何在容器里水平、垂直居中
第一种方法：<br>

```html
<div class="box">
    <img src="bigptr.jpg /><span></span>
</div>
```

<br>

```css
.box {width: 800px; height: 600px; border: 2px solid #000; text-align: center;}
span {display: inline-block; height: 100%; vertical-align: middle;}
img {vertical-align: middle;}
```

第二种方法：<br>
```html
<div class="box">
    <span><img src="bigptr.jpg /></span>
</div>
    ```
不考虑兼容的话，可以使用：<br>

```css
.box {width: 800px; height: 600px; border: 2px solid #000; display: table;}
span {display: table-cell; text-align: center; vertical-align: middle;}
```

考虑IE6、7兼容，则要写成：<br>
```css
.box {width: 800px; height: 600px; border: 2px solid #000; display: table; position: relative; overflow: hidden;}
span {display: table-cell; text-align: center; vertical-align: middle; *position: absolute; left：50%; top: 50%;}
img {*position: relative; vertical-align: top; left: -50%; top: -50%}
```
* 列表的文字溢出
li的里面分为左右两块元素，右边元素一直跟在左侧内容后边并距左侧元素10px间距。左侧元素宽度由左侧内容撑开。如果左右两侧内容总宽度超出了li宽度，就把左侧多出的文字隐藏掉。<br>
```html
<ul class="list">
    <li>
        <p>
            <a href="#">文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字</a>
            <span>文字</span>
        </p>
    </li>
    <li>
        <p>
            <a href="#">文字文字文字文字文字文字</a>
            <span>文字</span>
        </p>
    </li>
    <li>
        <p>
            <a href="#">文字文文字</a>
            <span>文字</span>
        </p>
    </li>
</ul>
```

<br>

```css
.list {width: 300pxp; margin: 0; padding: 0; list-style: none;}
li {height: 30px; font-size: 12px; line-height: 30px; border: 1px solid #000; overflow: hidden;vertical-align: top;}
span {padding: 10px;width: 40px; position: absolute; right: 0; top: 0;}
p {margin: 0; float: left; padding-right: 50px; position: relative;}
```

#### 整站规划
<br>
网站内文件夹的路径要固定<br>
首页一般命名为index.html（当用户访问服务器，默认是把index.html发送到客户端）<br>
要用英文命名<br>
对于中小型网站，首页和二级目录通常是放在根目录；如果页面比较多的话，可能会将网页放到文件夹内<br>
一般情况下，三级页面放在文件夹中<br>
css img js文件夹<br>
图片的划分有这样几种情况，一、统一放在img文件夹中；二、img里面只放img标签中的图片，背景图放在img下面的bg文件夹中<br>
css的划分的考虑<br>
网站的加载速度（一般一个优秀的网站打开要在5s之内，用户流失基本在1%以下。超过了5s之后，每秒1%-2%的用户流失量网上递增。超过30s，80%-90%的用户都会流失。）<br>
请求次数和服务器压力<br>
后期维护<br>
样式的通用性<br>
reset（样式重置）、public.css（公用样式）、index（首页私有样式区域）…… 其他私有样式区域<br>
css代码命名要带含义：根据每块元素的主题、功能、在页面上的位置进行命名。驼峰命名：从第二个单词开始每个单词的首字母大写。<br>
css代码，写包含样式的时候，能找到这个元素并且不影响其他元素即可<br>
常用命名法：<br>
<br>
页头：header 登陆条：loginBar 标志：logo 侧栏：sideBar 广告：banner 导航：nav 子导航：subNav 菜单：menu 子菜单：subMenu 搜索：search 滚动：scroll 页面主题：main 内容：content 标签页：tab 文章列表：list 提示信息：msg 小技巧：tips 栏目标题：title 加入：joinus 指南：guide 服务：service 热点：hot 新闻：news 下载：download 注册：register 状态：status 按钮：btn 投票：vote 合作伙伴：partner 友情链接：friendLink 页脚：footer 版权copyRight 外套：wrap 商标：label 顶导航：topnav 边导航：sidebar 左导航；leftsideBar 右导航：rightsideBar 注释：note 面包屑：breadCrumb（即页面所处位置导航提示） 容器：container 内容：content 当前：current<br>
避免命名冲突，在私有样式区域，给每个私有样式区域的样式都固定一个字母前缀<br>
<br>
* 样式重置
方法一（代码简化、开发麻烦）：遇到一个标签，就重置一个标签的样式<br>
方法二：直接复制其他网站的样式重置（有些标签没用到，有些标签不符合自己的项目需求），这需要在其它网站的重置样式表上进行调整。<br>

```css
body, h1, h2, h3, h4, h5, h6, p, dl, dd, ul, ol, pre, form, input, textarea, th, td, select {margin: 0; padding: 0;}
em {font-style: normal;}
li {list-style: none;}
a {text-decoration: none;}
img {border: none; vertical-align: top;}
table {border-collapse: collapse;}
textarea {resize: none; overflow: auto;}
```

页面宽度指的是页面内容的宽度，而不是设计图的宽度<br>
最好不要把所有内容放在一个div里面，最好分开来写<br>
最好不要写成：<br>
```html
<div class="wrap">
    <div class="header"></div>
    <div class="nav"></div>
    <div class="main"></div>
    <div class="footer"></div>
</div>
```
浏览器解析是从上往下解析，碰到一个标签就把里面的标签全部加载然后再显示在页面上。如果把body里面所有内容都包在一个div里面，那么如果页面很长的话，浏览器显示的页面会很长时间什么也显示不出来，然后突然所有内容冒出来了，效果不好。<br>
<br>
最好分开来写：<br>
```html
<div id="header">
    <div class="header wrap"></div>
</div>
<ul id="nav" class="wrap"></ul>
<div id="picTab" class="wrap">
    <div class="picTab wrap"></div>
</div>
<div id="whyQQ" class="wrap"></div>
<div id="main" class="wrap"></div>
<div id="footer" class="wrap"></div>
```
然后给加了wrap类的内容加样式，宽960居中。<br>
<br>
标签页上的小图标的制作<br>
<br>
用ico在线制作工具<br>
```html
< link href=”favicon.ico” rel=”icon” />
```
