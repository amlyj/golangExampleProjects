# pipeline
> 使用go语言搭建一个并行处理管道，处理大文件进行排序操作,
> 注：本项目代码学习参考自.慕课网教学视频

## 知识点
* go routine

* 归并排序
> 将数据分为左右两半，分别归并排序，再把两个有序的数据归并（取队头元素进行比较，取出其中最小值，循环此步骤直至取完.）

* 文件切分，多路合并
> 将文件分为多块，使每一块都能在内存中排序，都排完之后，数据归并，针对于特别大的文件，我们只需取数据的队头元素即可，
> 所以归并排序可以处理大文件操作。

* 文件读写

* 节点调用
> goroutine之间通过channel来进行通信，类似Java中进程间的RPC方法调用。