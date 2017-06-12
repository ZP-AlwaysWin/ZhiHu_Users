1.创建项目
scrapy startproject zhihuuser

2.接下来我们需要创建一个spider，同样利用命令行，不过这次命令行需要进入到项目里运行。
cd zhihuuser
scrapy genspider zhihu www.zhihu.com


3.https://www.zhihu.com/robots.txt

User-agent: *
Crawl-delay: 10

Disallow: /login
Disallow: /logout
Disallow: /resetpassword
Disallow: /terms
Disallow: /search
Disallow: /notifications
Disallow: /settings
Disallow: /inbox
Disallow: /admin_inbox
Disallow: /*?guide*
Disallow: /people/*-*-*-*

4.
当然我们现在运行的是单机爬虫，只在一台电脑上运行速度是有限的，所以后面我们要想提高抓取效率，需要用到分布式爬虫，
在这里需要用到Redis来维护一个公共的爬取队列。