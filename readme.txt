# spidermain
主要是分为4个模块
1.爬虫调度端
启动爬虫，停止爬虫，或者监视爬虫的运行情况。 
我们以百度百科python词条的url为入口。编写主函数
2.url管理器
管理待抓取url集合和已抓取的url集合，目的防止重复抓取，循环抓取，需要支持的方法：
判断待爬取url是否在容器中
添加新url到待爬取集合中
判断是否还有待爬取的url
获取待爬取url
将url从待爬取移动到已爬取 
根据方法编写对应的代码。
3.网页下载器
从待爬去的url管理中取出一个url，下载器会将url指定的网页下载下来，存储成一个字符串。 
这里用到了python的urllib.request库，实现网页的下载。
4.网页解析器
将字符串传送给网页解析器，一方面解析出有价值的数据，一方面将网页中指向其他网页的url补充给url管理器，形成循环。 
这里用到了结构化解析,BeautifuSoup就是使用DOM树的方式来解析网页的。