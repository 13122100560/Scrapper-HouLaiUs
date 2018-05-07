# 概要说明：
本库尝试爬取豆瓣上《后来的我们》的热门短评，包括：

* 评论（文字）
* 评分（星星数）
* 该评论的有用程度
* 评论发布时间

# 文件解释：


|    文件    | 内容 |
| ---------- | --- |
| comment.csv |  爬取的所有热门评论结果 |
| proxies.csv       |  爬取的代理IP，供编制爬虫的时候使用 |
| scrapper-bs4.ipynb |  爬虫主体，使用BeautifulSoup+re抽取字段 |
| proxy.ipynb |  爬取代理IP的爬虫 |
| re.txt  |  Python库要求 |

# 使用方法：
使用版本：Python 2.7.5(所有语法遵循Python3规范)

1、安装必要的Python库

```
python install -r re.txt -i http://pypi.douban.com/simple --trusted-host pypi.douban.com
```
安装后再Clone的库下执行以下命令启动jupyter
```
jupyter notebook
```

2、爬取代理IP

从上到下执行`proxy.ipynb`每个Cell中的代码即可。

3、爬取短评

从上到下执行`scrapper-bs4.ipynb`每个Cell中的代码即可。

# 爬取结果展示：


![](https://github.com/XiaohuiLee/Scrapper-HouLaiUs/blob/master/comments.png)

接下来的下一步计划：
我接下来会尝试对爬取的数据做可视化的展现，包括评分分布，时间序列分析，以及对热评的频率分析
