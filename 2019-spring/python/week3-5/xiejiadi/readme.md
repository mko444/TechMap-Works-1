# week3-5 python爬虫

## 学习到的东西

1. 学习了如何使用requests库，比如用get（url）命令可以快速地获得网页的源代码，从而进行文本的匹配，提取信息。

2. 通过观察豆瓣排行榜的网址（"https://movie.douban.com/top250?start=25&filter="）发现不同页数之间的区别仅仅是“？start=”后面的数字，从而通过修改数值可以方便地进行翻页。

3. 本次练习中通过使用正则表达式匹配页面文本，更加直观地了解了正则表达式的适用情形，也了解了更多正则表达式不同的写法。

## 出现的问题及解决

1. 在一开始的用正则表达式匹配文本时出现匹配不到文本的错误，因为一开始是参照网上的案例写的匹配式，所以不是特别理解，后来通过查找资料和试验解决了问题。

2. 匹配完文本后发现电影简介里出现了“\n”"< br />""\u3000\u3000"以及空字符等不想要的字符，在群里讨论后智杰告诉我可以用replace和strip（）等方法来去除空字符，但因为我是list格式，所以无法使用，在网上查找后知道了使用“string_name = ''.join(list_name)”的方式来将list格式转换为字符串格式。

3. 在pycharm中使用strip（）以及replace（）等命令时发现没有效果，而在IDE环境中可行，导致困惑，在后来的实践中意识到，replace（）和strip（）等命令并不改变变量本身，因此需要将处理后的结果赋值给另一个变量来保存。即"string1 = string.replace()"

4. 然而strip（）命令只能去除头尾的空字符，句中的空字符却无法去除，在网上查找解决方法时，知道了可以通过replace(' ','')来将句中所有的空字符去除。