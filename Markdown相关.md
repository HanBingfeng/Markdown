# Markdown项目个人工作记录 #
```该文档为个人的工作记录```
>***2018.09.05***:   
>>**什么是Markdown**：  
    &emsp;&emsp;Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。  
    &emsp;&emsp;Markdown具有一系列衍生版本，用于扩展Markdown的功能（如表格、脚注、内嵌HTML等等），这些功能原初的Markdown尚不具备，
它们能让Markdown转换成更多的格式，例如LaTeX，Docbook。Markdown增强版中比较有名的有Markdown Extra、MultiMarkdown、 Maruku等。  
    &emsp;&emsp;这些衍生版本要么基于工具，如Pandoc；要么基于网站，如GitHub和Wikipedia，在语法上基本兼容，但在一些语法和渲染效果上有改动。</br>  
**我们要做什么**：</br>
  &emsp;&emsp;`文本编辑器`  VS  `具有衍生功能的文本编辑器(扩展Markdown)`   
  &emsp;&emsp;基于对Latex和HTML等标记性语言的理解和应用，制作简单的文本编辑器可行性较高。</br>
  &emsp;&emsp;*扩展功能基于工程进度安排。*</br>  
**怎么做**：<table>
    <th>工作安排</th><th>工作量占比分析</th>
    <tr><td>了解熟悉Markdown语言的语法规则和功能</td><td>10%</td></tr>
    <tr><td>设计Markdown标记语言的实现方案</td><td>10%</td></tr>
    <tr><td>设计编译器用户UI</td><td>10%</td></tr>
    <tr><td>完成编码</td><td>50%</td></tr>
    <tr><td>测试完善</td><td>20%</td></tr>
    </table>
**需要搞明白的问题**：  
  &emsp;&emsp;***1***.如何制作编译器的图形界面，即窗口、按钮等，以及最重要的 如何生成目标文档。  
  &emsp;&emsp;***2***.如何分配窗口，都有哪些功能。  
  &emsp;&emsp;***3***.作为一个编译器，快捷键如何实现。  
  &emsp;&emsp;***4***.参考 MarkdownPad，VSCode等现有编译器，需要实现(copy)哪些功能。  

>***2018.09.06***
>>**Markdown原理**：  
    &emsp;&emsp;将Markdown文本编辑器中的语言转换为HTML语言，并在网页中生成目标文档。
    </br>&emsp;&emsp;其中，各个模块的CSS时可自行设计的。</br>   
**参考Markdown编译器**：  
    &emsp;&emsp;1.MarkdownPad2  
    &emsp;&emsp;2.['马克飞象'](https://maxiang.io/)  
    &emsp;&emsp;3.['简书'](https://www.jianshu.com/)    
  </br>```注：其中简书不支持内嵌HTML，即不可以直接使用HTML文法。同时没种编译器在markdown语法上有细微的差异，比如标题"#"前后是否有空格。```
  
>***2018.09.08***
>>**Markdown版需求分析**：  
链接：[需求分析](https://github.com/HanBingfeng0221151602/Markdown/blob/master/%E3%80%90%E5%BC%80%E5%8F%91%E6%96%87%E6%A1%A301%E3%80%91%E9%9C%80%E6%B1%82%E5%88%86%E6%9E%90.md)  

>***2018.09.13***
>>**概要设计(用户使用说明)**:  
链接：[概要设计](https://github.com/HanBingfeng0221151602/Markdown/blob/master/%E3%80%90%E5%BC%80%E5%8F%91%E6%96%87%E6%A1%A302%E3%80%91%E6%A6%82%E8%A6%81%E8%AE%BE%E8%AE%A1.md)  

><a name="20180916"></a>***2018.09.14***  
>>**完善编辑器界面**  

>***2018.09.16***  
>>**Markdown文法分析**：<table>
<th>类别</th><th>子类别</th><th>Markdown文法</th><th>HTML文法</th>
    <tr><td rowspan="6">标题</td><td>一级标题</td><td># 标题 #</td><td>&#60;h1&#62;标题&#60;/h1&#62;</td></tr>
    <tr><td>二级标题</td><td>## 标题 ##</td><td>&#60;h2&#62;标题&#60;/h2&#62;</td></tr>
    <tr><td>三级标题</td><td>### 标题 ###</td><td>&#60;h3&#62;标题&#60;/h3&#62;</td></tr>
    <tr><td>四级标题</td><td>#### 标题 ####</td><td>&#60;h4&#62;标题&#60;/h4&#62;</td></tr>
    <tr><td>五级标题</td><td>##### 标题 #####</td><td>&#60;h5&#62;标题&#60;/h5&#62;</td></tr>
    <tr><td>六级标题</td><td>###### 标题 ######</td><td>&#60;h6&#62;标题&#60;/h6&#62;</td></tr>
    <tr><td rowspan="4">文本字体</td><td>斜体</td><td>*文本*</td><td>&#60;i&#62;文本&#60;/i&#62;</br>&#60;em&#62;文本&#60;/em&#62;</td></tr>
    <tr><td>加粗</td><td>**文本**</td><td>&#60;b&#62;文本&#60;/b&#62;</br>&#60;strong&#62;文本&#60;/strong&#62;</td></tr>
    <tr><td>斜体加粗</td><td>***文本***</td><td>综合使用以上<i>斜体</i>和<b>加粗</b>标签</td></tr>
    <tr><td>删除线</td><td>~~文本~~</td><td>&#60;s&#62;文本&#60;/s&#62;</td></tr>
    <tr><td colspan="2">引用</td><td>&#62;及多个&#62;</td><td>&#60;blockquote&#62;引用内容&#60;/blockquote&#62;</br>(可以嵌套)</td></tr>
    <tr><td colspan="2">分割线</td><td>三个及三个以上 * 或 -</td><td>&#60;HR&#62;</br>(具体样式可用CSS自行设置)</td></tr>
    <tr><td colspan="2">图片</td><td>![图片名字](图片链接)</td><td>&#60;img /&#62;(图片默认原始大小，没有位置样式)</td></tr>
    <tr><td colspan="2">超链接</td><td>[链接名字](链接地址)</td><td>&#60;a href="链接地址"&#62;链接名字&#60;/a&#62;</td></tr>
    <tr><td rowspan="2">列表</td><td>无序列表</td><td>- * +符号中任意一个`_`文本</br>(`_`表示一个空格)</td><td>&#60;ul&#62;</br>&#60;li&#62;&#60;/li&#62;</br>……</br>&#60;/ul&#62;</td></tr>
    <tr><td>有序列表</td><td>1.</br>2.</br>……</td><td>&#60;ol&#62;</br>&#60;li&#62;&#60;/li&#62;</br>……</br>&#60;/ol&#62;</td></tr>
    <tr><td colspan="2">表格</td><td>| header1 | header2 | header3 |</br>|:----|:----:|----:|</br>|content1|content2|content3|</td><td>&#60;table&#62;</br>&#60;th&#62;表头&#60;/th&#62;</br>&#60;tr&#62;&#60;td&#62;&#60;/td&#62;&#60;/tr&#62;</br>……</br>&#60;/table&#62;</td></tr>
    <tr><td rowspan="2">代码块</td><td>单行代码</td><td>`文本`</td><td>&#60;code&#62;文本&#60;/code&#62;</td></tr>
    <tr><td>多行代码</td><td>```</br>代码块内容</br>```</td><td><B>难题一</B></td></tr>
    <tr><td colspan="2">HTML语言内嵌的识别</td><td>HTML语言的标签及内容</td><td>识别&#60;和&#62;的标签标志及标签内容</td></tr>
    <tr><td colspan="2">数学公式</td><td colspan="2"><B>难题二</B></td></tr>
    <tr><td colspan="2">流程图</td><td colspan="2"><B>难题三</B></td></tr>
</table>
