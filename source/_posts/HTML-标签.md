---
title: HTML-标签
date: 2017-11-29 02:08:04
tags:
---

刚接触 HTML，了解了一些标签的用法，举一些常见的标签来说一下。
1、iframe 标签
    - 其实 iframe 标签在现在已经很少被大范围的使用了，就简单说几个常用
      的方法。
    - iframe 主要是用来嵌套页面的
	- <iframe src="https://www.baidu.com" name="xxx"></iframe>
	- 这是 iframe 最基础的用法，用于在页面中放入 src 属性指向的页
	  面
    iframe 标签与 a 标签结合用的比较多，现在先介绍一下 a 标签
2、a 标签
    - a 标签用于跳转页面，发出 HTTP 的 GET 请求
	- 属性见 MDN：https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a
    - a 标签的 target 属性：
	- target="_blank"：表示新的页面会在新建的空页面打开
	- target="_self"：表示新的页面会在当前页面打开
	- target="_parent"：表示新的页面会在父页面打开
	- target="_top"：表示新的页面会在顶层窗口打开
    - a 标签的 download 属性：
	- 一个链接可以下载有两种方式：
	    - 后端程序猿使用 Content-Type 属性，将其设置为：
	      application/cotet-stream
	    - 在 a 标签中使用 download 属性，注明其是一个下载链接
    - a 标签的 href 地址格式：
	- href="//qq.com"：这是一个无协议绝对地址，他会自动继承父元素
	  的目录
	- href="xxx.hmtl"：会跳转到 xxx.html，只以此目录为参考，其中
	    - href="#ssss"：会加入到地址栏路径之后，不会发起请求
	    - href="?name=frank"：会加入到地址栏的路径之后，但是它同时
	      会发起请求
	- href="javascript:;"：这是一个 javascript 伪协议，如果一个 a
	  标签元素设置了这个属性，那么点击它，它并不会跳转，以此来达到
	  某些目的
3、iframe 标签和 a 标签一起使用的话：
    - <body>
	<iframe name=xxx src="#" frameborder="0"></iframe>
	<a target=xxx href="http://qq.com">QQ</a>
	<a target=xxx href="http://baidu.com">百度</a>
      </body>
    - 在上例中，在主页面会开一个iframe窗口，frameborder是窗口的边框，
      如果不设置成0的话，会看到一个不太好看到边框，所以一般都设置成0
    - a 标签的 target 属性，对应的是 iframe 标签的 name 属性的值，所以
      我们会在 iframe 窗口打开上述这两个网站
4、form 标签
    - form 标签也会实现页面跳转，通常是发出 HTTP POST 请求
	- form 标签的详细属性见 MDN：https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/form
    - form 有一个很重要的特点，如果这个表单里面没有提交按钮的话，就无
      法提交这个表单
    - form 标签主要是用来发起 POST 请求的。form 标签的 method 属性，只
      能写两种方法 —— GET 和 POST，一般不会用 GET。GET 方法会把参数
      加到查询参数里
    - form 中的 input 标签里的 name 属性，你会在 Form Data 里看到
    - 这个时候也需要讲一下 button 标签，button 标签与 form 标签结合起
      来用的话，要注意两点：
	- 如果你的 form 标签里面写了一个没有 type 属性的 button 标签，
	  那么 button 标签会自动升级为提交按钮
	- 如果你的 form 标签里写了一个有 type 属性的 button 标签，并且
	  它的 type 属性不是 submit 的话，那么，button 标签就不会自动
          升级成提交按钮
5、input / button 标签
    - input / botton 标签的区别：是否为[空标签]
	- 意思就是，input 标签里面不能有子标签，button 标签里可以有子
	  标签
    - input 的属性见 MDN：https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input
    - button 的属性见 MDN：https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button
    - <input type="button" value="button">
	- input 和 label 标签使用：
	    - <input type="checkbox" id="xxx"><label for="xxx">爱我
	      </label>：此时，表示的是 label 标签是 input 标签所选择的
	      东西
	    - 也可以这样写：<label>用户名<input type="text" name="xxx"></label>：
	      这里用 label 标签将 input 标签包起来，如果你选中的是文字
	    ，也会选中前面的选项
	- input 的 type 如果是 radio:
	    - <label><input name="loveme" type="radio" value="yes">Yes</label>
	      <label><input name="loveme" type="radio" value="no">No</label>
	    - 如果两个 radio 按钮有同一个 name 的话，就只能选一个
	- <select name="group" multiple>
	    <option value="">-</option>
	    <option value="1">第一组</option>
	    <option value="2">第二组</option>
	    <option value="3" disabled>第三组</option>
	    <option value="4" selected>第四组</option>
	    - 这里，是一个下拉选择框，multiple 属性表示是多选；
	      disabled 属性表示不能选；selected 属性表示默认选中
	- <textarea style="resize:none; width: 200px heigth: 100px;"
	  name="爱好" cols="30" rows="10"></textarea>
	    - 这是用来写多行文字的，textarea 标签属于可替换标签，它自
	      带宽高，但是可以使用属性设置或者 CSS 将其覆盖
	    - 这里设置的 cols 在实际运用中不一定是这么多格，但是 rows
	      是一定是这么多格
6、table 标签
    - table 标签用于展示数据，属性见：https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/table
    - table 标签里只能出现这几个标签：<thead>、<tbody>、<tfoot>
	- thead，tbody、tfoot 标签里面可以有：<tr>(table row)、
	  <th>(table header)、<td>(table data) 这几个标签
    - <colgroup>
	<col width=100>
	<col width=200>
      </colgroup>
	- 这个标签，现在用的比较少了，他是用来列列指定表格每一列的宽度
    - 不管 <thead>、<tbody>、<tfoot> 标签的前后顺序如何，浏览器都会按
      照 head、body、foot 的顺序来显示它

HTML 的标签实在是太多太复杂，要想好好掌握，必须得多多实践才好，今天就
暂时了解到这里

