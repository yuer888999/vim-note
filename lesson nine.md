# Vim复制粘贴与寄存器的使用 
## Vim Normal模式复制粘贴  
### 初学者会感觉Vim复制粘贴比较奇怪，先从normal模式学习  
normal模式下复制粘贴分别使用y(yank)和p(put),剪贴 d 和 p  
我们可以使用 v(visual) 命令选中所要复制的地方，然后使用p粘贴  
配合文本对象：比如使用yiw复制一个单词，yy复制一行  
## Insert模式下的复制粘贴  
### 很多人使用鼠标进行选中，然后使用 ctrl+v 或者 cmd+v 粘贴  
这个和其他的文本编辑器差不多，但是粘贴代码有个坑  
很多人在vimrc中设置了 autoindent ,粘贴Python 代码缩进错乱  
这个时候需要使用 :set paste 和 :set nopaste 解决  
# 什么是Vim的寄存器 
### 你有没有好奇？Vim在normal模式下复制/剪贴的内容去了哪？ 
Vim里操作的是寄存器而不是系统剪贴板，这和其他编辑器不同  
默认我们使用d删除或者y复制的内容都放到了“无名寄存器”  
用x删除一个字符放到无名寄存器，然后p粘贴，可以调换两字符  
## 深入寄存器(register)  
### Vim不使用单一剪贴板进行剪贴，复制与粘贴，而是多组寄存器 
通过 "{register} 前缀可以指定寄存器，不指定默认用无名寄存器  
比如使用 "ayiw复制一个单词到寄存器a中，"bdd删除当前行到寄存器b中  
Vim中 "" 表示无名寄存器，缺省使用。 "" p其实就等同p  
## 其他常用寄存器 
### 出了有名寄存器 a-z ,Vim中还有一些其他常用寄存器 
复制专用寄存器 "0使用y复制文本同时会被拷到复制寄存器0  
系统剪贴板 "+可以在复制前加上 "+复制到系统剪贴板  
其他一些寄存器比如 %当前文件名，".上次插入的文本  




# :echo has('clipboard') 查看是否有系统剪贴板，返回值为 1 有系统剪贴板  
# :set clipboard=unnamed可以让你直接复制粘贴系统剪贴板内容  
