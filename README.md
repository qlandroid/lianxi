# android-function
添加了WebView的使用，WebView 的基本属性已经填加注解，在WebView中播放视频时，全屏显示 与取消全屏显示；
第二个页面可以测试取消通知栏，哪个属性实现什么样的功能；
第三个页面添加图片的压缩功能；
第四个页面添加了异步处理，网络下载，图片的三级缓存；
图片的三级缓存，使用LruCache + softReference软引用+ 本地+ 网络；
图片控缓存，使用的网络下载很简易，有时间研究网络下载的框架重新编写，图片缓存，还差一个控制图片加载内存大小的回调方法，和默认的方法，目前加载的图片质量为，网络下载图片的原始大小；
异步处理，使用了线程池，handler，信号量semaphore 等，控制工作线程，引入栈，队列；栈，先进后出；队列，先进先出；控制图片的加载顺序；
使用pullToRefrechListView，
listView的自己编辑万能适配器，解决复用问题引起的图片错乱，解决数据加载时，刷新适配器引起的闪屏问题；
使用listView的时候，滑动时不加载图片，这样可以解决滑动时带来的卡顿；
所以合理的使用控制加载图片的状态，可以带来更好的用户体验；
一直监控第四个布局产生的内存，在关闭后该页面后，内存释放的快，内存保持平稳；
