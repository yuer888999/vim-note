# Vim模式
### vim和其他很多编辑器的区别在于多种模式

进入Vim默认是normal(普通)模式？为什么不是编辑模式呢
使用a(sppend)i(insert)等进入编辑器模式
还有:cmd命令模式和v(isual)可视化模式i

###为什么进入Vim不是插入-normal模式
####奇怪的是，为什么vim进入之后不像其他编辑器一样直接插入？
进入vim默认是normal(普通)模式，使用Esc从插入回到普通模式。
普通模式下可以进入各种命令操作和移动
大部分情况下你是在浏览而不是编辑，所以Vim默认是normal
#Insert(插入)模式
###插入模式下Vim可以直接编辑，和其他编辑器一样
使用i(insert) a(append) o(open a line below)进入插入模式
使用Esc退出插入到normal模式
你来试试I，A，O如何进入插入模式的？
##Command(命令)模式
###模式下输入：之后执行命令，比如保存退出 :wq 一气呵成
顾名思义，执行Vim命令，比如保存 :w , 退出 :q
比如分屏 ;vs(vertical split), :sp(split)
比如使用 :% s/foo/bar/g 全局替换
##Visual(可视)模式
###Visual模式一般用来块状选择文本
Normal模式下使用v进入visual选择
使用V选择行
使用 ctrl+v 进行方块选择