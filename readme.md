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
| visualization.ipynb |  《后来的我们》的数据可视化 |
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

4、数据可视化
从上到下执行`visualization.ipynb`每个Cell中的代码即可。
# 爬取结果展示：


![](https://github.com/XiaohuiLee/Scrapper-HouLaiUs/blob/master/comments.png)


# 可视化结果展示：
![评价情况分布1](https://github.com/XiaohuiLee/Scrapper-HouLaiUs/blob/master/viz1.png)
![评价情况分布2](https://github.com/XiaohuiLee/Scrapper-HouLaiUs/blob/master/viz2.png)
![打分随时间分布情况](https://github.com/XiaohuiLee/Scrapper-HouLaiUs/blob/master/viz3.png)
![《后来的我们》词云图1](https://github.com/XiaohuiLee/Scrapper-HouLaiUs/blob/master/viz4.png)
![《后来的我们》词云图2](https://github.com/XiaohuiLee/Scrapper-HouLaiUs/blob/master/wordCloud.png)


>接下来的下一步计划：我接下来会尝试对爬取的数据做可视化的展现，包括评分分布，时间序列分析，以及对热评的频率分析

# 总结结论：
在对豆瓣上对于《后来的我们》进行热门短评爬取过后，看起来《后》的确口碑不佳。

1、前十热门短评只有一条表达了较为正面的意见

2、有过半数的影迷给出了差评的评价

3、大家对于`刘若英`和`冬雨`的话题热度比较高，可能是因为这是奶茶的电影首秀，大家对周冬雨的演技也开始有所看好。

4、词云中看出大家对该片的反映可能还不是很热情，“尴尬”，“退票”，“垃圾”，“呵呵”这一类比较贬义的词出现的次数也比较高
