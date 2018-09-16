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

>***2018.09.14***  
>>**完善编辑器界面**  

>***2018.09.16***  
>>**Markdown文法分析**：  
