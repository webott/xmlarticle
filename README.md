 QQ：2645542961 
   今天主要讲发送xml消息，分析找到发送的call，就是转发文章的。附近OD，附加CE，然后在公众号找一篇文章，右键点击转发，比如转发给文件助手，然后把文件助手的wxid，修改一下，然后搜索一下，出来3个结果，
![image](https://user-images.githubusercontent.com/73727649/118383808-e36b9d00-b633-11eb-807c-9ea25418c00c.png)
然后拿一个地址，在OD里面下一个内存访问断点，
![image](https://user-images.githubusercontent.com/73727649/118383812-e9617e00-b633-11eb-982d-78d1e47a9fe4.png)
然后在微信点击确定转发，断点断下来了，然后删除内存访问断点，在反汇编里面看，下一个断点，即左上角放一个断点，然后一直单步运行，这个转发至少是需要三个参数，即：转发给谁，发送的内容，从哪里发送；然后找到有这三个参数的地方，下个断点。
![image](https://user-images.githubusercontent.com/73727649/118383814-ef575f00-b633-11eb-8a15-8a09099e507c.png)
直接运行过去，然后在微信再转发一次，看是否断下来，发现断点断下来了，然后把里面的发送内容，在内存里面改个字，然后再运行过去，然后看下转发的字是否改成功。发现更改成功，说明就是这个call。
![image](https://user-images.githubusercontent.com/73727649/118383815-f8483080-b633-11eb-8196-48e14d20207e.png)
现在已实现各种有趣的功能，发送各种消息，下载各种文件，转发信息，接收各种消息，群管等功能，支持各种开发语言二次开发，欢迎技术交流。
![image](https://user-images.githubusercontent.com/73727649/118383828-1746c280-b634-11eb-80be-6f08581f9d1a.png)

