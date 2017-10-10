## task01九宫格
1.文档声明头 此标签可告知浏览器文档使用哪种 HTML 或 XHTML 规范<br>
<!DOCTYPE> 声明不是 HTML 标签；它是指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的指令。<br>
DOCTYPE标签是一种标准通用标记语言的文档类型声明，它的目的是要告诉标准通用标记语言解析器，它应该使用什么样的文档类型定义（DTD）来解析文档。<br><br>

在 HTML 4.01 中，<!DOCTYPE> 声明引用 DTD，因为 HTML 4.01 基于 SGML。DTD 规定了标记语言的规则，这样浏览器才能正确地呈现内容。<br>
HTML5 不基于 SGML，所以不需要引用 DTD。<br>
提示：请始终向 HTML 文档添加 <!DOCTYPE> 声明，这样浏览器才能获知文档类型。<br><br>

2.XHTML介绍：<br>
XHTML：Extensible Hypertext Markup Language，可扩展超文本标注语言。<br>
XHTML的主要目的是为了取代HTML，也可以理解为HTML的升级版。<br>
HTML的标记书写很不规范，会造成其它的设备(ipad、手机、电视等)无法正常显示。<br>
XHTML与HTML4.0的标记基本上一样。<br>
XHTML是严格的、纯净的HTML。<br><br>

编写XHTML的规范：<br>
（1）所有标记元素都要正确的嵌套，不能交叉嵌套。<br>
（2）所有的标记都必须小写。<br>
（3）所有的标记都必须关闭。<br>
双边标记：<span></span><br>
单边标记：<br> 转成 <br /> <hr> 转成 <hr />还有<img src=“URL” /><br>
（4）所有的属性值必须加引号。<font color="red"></font><br>
（5）所有的属性必须有值。<hr noshade="noshade">、<input type="radio" checked="checked" /><br>
（6）XHTML文档开头必须要有DTD文档类型定义<br><br>

3.http：超文本传协议。用来规定客户端浏览器和服务端交互时数据的一个格式。SMTP 邮件传输协议，ftp:文件传输协议。<br><br>

4.<meta http-equiv="refresh" content="3;http://www.baidu.com"><br>
上面这个标签的意思是说，3秒之后，自动跳转到百度页面。<br><br>

5.字符集 charset<br>
UTF-8：字多，有各种国家的语言，但是保存尺寸大，文件臃肿；<br>
gb2312：字少，只用中文和少数外语和符号，但是尺寸小，文件小巧。<br><br>

6.SEO<br>
<meta name="Description" content="网易是中国领先的互联网技术公司，为用户提供免费邮箱、游戏、搜索引擎服务，开设新闻、娱乐、体育等30多个内容频道，及博客、视频、论坛等互动交流，网聚人的力量。" /><br>
只要设置的Description页面描述，那么百度搜索结果，就能够显示这些语句，这个技术叫做SEO（search engine optimization，搜索引擎优化）。<br>
<meta name="Keywords" content="网易,邮箱,游戏,新闻,体育,娱乐,女性,亚运,论坛,短信" /><br>
这些关键词，就是告诉搜索引擎，这个网页是干嘛的，能够提高搜索命中率。让别人能够找到你，搜索到你。<br><br>

7.面试题：<br><br>

问：网页的head标签里面，表示的是页面的配置，有什么配置？<br>
答：字符集、关键词、页面描述、页面标题。（今后我们还能看见一些其他的配置：IE适配、视口、iPhone小图标等等）<br><br>

8.viewport<br>
一个常用的针对移动网页优化过的页面的 viewport meta 标签大致如下：<br>
<meta name="viewport" content="width=device-width, initial-scale=1.0"><br>
width：控制 viewport 的大小，可以指定的一个值，如 600，或者特殊的值，如 device-width 为设备的宽度（单位为缩放为 100% 时的 CSS 的像素）。<br>
height：和 width 相对应，指定高度。<br>
initial-scale：初始缩放比例，也即是当页面第一次 load 的时候缩放比例。<br>
maximum-scale：允许用户缩放到的最大比例。<br>
minimum-scale：允许用户缩放到的最小比例。<br>
user-scalable：用户是否可以手动缩放。<br>
