1.该文件夹下所有的文件例子，都是基于宋宝华《linux设备驱动程序开发详解，基于最新4.0内核》写的，所有的代码都经过了调试和验证并附有log文档。
2.globalfifo是在堆内存里面通过kzalloc()函数申请的一段内存，符合fifo的先进先出属性，但并不是循环缓冲区。当该内存被读出n个字节后剩下的字节会被复制到fifo的首地址，实现较简单（可能考虑到读者水平参差，原书也是这么做的）。