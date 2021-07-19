# 什么是Vim 的 text object  
## 如果你学过主流的编辑器语言，一定知道面向对象编程  
Vim里文本也有对象的概念，比如一个单词，一段句子，一个段落  
很多其他编辑器经常只能操作单个字符来修改文本，比较低效  
通过操作文本对象修改要比只操作单个字符高效  
### 文本对象操作方式  
### 之前我们已经使用过文本对象，回忆下 dw (删除一个单词)  
[number]<command>[text object]  
number表示次数，command是命令，d(elete),c(hange),y(ank)  
text object是要操作的文本对象，比如单词w,句子s,段落p  

