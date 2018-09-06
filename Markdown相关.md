# Markdown项目个人工作记录 #
```该文档为个人的工作记录```
---
>***2018.09.05***:   
>>**什么是Markdown**：  
    &emsp;&emsp;Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。  
    &emsp;&emsp;Markdown具有一系列衍生版本，用于扩展Markdown的功能（如表格、脚注、内嵌HTML等等），这些功能原初的Markdown尚不具备，
它们能让Markdown转换成更多的格式，例如LaTeX，Docbook。Markdown增强版中比较有名的有Markdown Extra、MultiMarkdown、 Maruku等。  
    &emsp;&emsp;这些衍生版本要么基于工具，如Pandoc；要么基于网站，如GitHub和Wikipedia，在语法上基本兼容，但在一些语法和渲染效果上有改动。</br>  
**我们要做什么**：</br>
  &emsp;&emsp;*文本编辑器*  VS  *具有衍生功能的文本编辑器(扩展Markdown)*   
  &emsp;&emsp;基于对Latex和HTML等标记性语言的理解和应用，制作简单的文本编辑器可行性较高。</br>
  &emsp;&emsp;*扩展功能基于工程进度安排。*</br>  
**怎么做**：  
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
  ·MarkdownPad2  
  ·[马克飞象](https://maxiang.io/)  
  ·简书  
  ```注：其中简书不支持内嵌HTML，即不可以直接使用HTML文法。同时没种编译器在markdown语法上有细微的差异，比如标题"#"前后是否有空格。```
  
