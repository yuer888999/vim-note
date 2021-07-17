# Vim如何搜索替换 
## Vim替换命令 
substitute命令允许我们查找并且替换掉文本，并且支持正则式   
:[range]s[ubstitute]/{pattern}/{string}/[flags]  
range表示范围 比如：10，20表示10-20行，%表示全部  
pattern是要替换的模式，string是替换后文本  
#####  flags有几个常用的标志 
g(global)表示全局内执行  
c(confirm)表示确认，可以确认或者拒绝修改  
n(number)报告匹配到的次数而不替换，可以用来查询匹配次数 

