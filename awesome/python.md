[TOC]
Python应用生态
https://www.pythonstacks.com/

## 自动化
### automagica
https://github.com/automagica/automagica 3.1k

## 爬虫

### 爬虫工具箱
https://github.com/kangvcar/InfoSpider

**数据源**
- GitHub
- QQ邮箱
- 网易邮箱
- 阿里邮箱
- 新浪邮箱
- Hotmail邮箱
- Outlook邮箱
- 京东
- 淘宝
- 支付宝
- 中国移动
- 中国联通
- 中国电信
- 知乎
- 哔哩哔哩
- 网易云音乐
- QQ好友
- QQ群
- 生成朋友圈相册
- 浏览器浏览历史
- 12306
- 博客园
- CSDN博客
- 开源中国博客
- 简书

**数据分析**
- 博客园
- CSDN博客
- 开源中国博客
- 简书

### 通过用户名在社交网络上搜索社交媒体账户
https://github.com/sherlock-project/sherlock

### Photon
GitHub链接：https://github.com/s0md3v/Photon

Photon 是一个使用 Python 构建的功能强大且易于使用的 web 爬虫程序。
s0md3v 的轻量级和快速爬虫遵循开源智能框架的指导方针和方法，该框架允许收集和分析从开放或公共来源获取的信息。

Photon 可以从中抓取信息的许多来源包括：
- URL，包括带参数的URL
- 社交媒体账户、电子邮件
- pdf、png、XML文档等文件
- 子域
- JavaScript文件

Photon 以有组织的方式保存所有提取的信息，甚至可以导出为 JSON 文件。该工具还提供了各种选项来自定义它的工作方式，比如控制超时，排除一些 url 等等。
## 服务器操作
### paramiko
一个可用于渗透测试人员和软件开发人员的交互式tls拦截HTTP代理。
https://github.com/paramiko/paramiko

## 网络
### mitmproxy
https://github.com/mitmproxy/mitmproxy

## Tools
### 图片
- [Haishoku - 自动化图表配色](https://github.com/LanceGin/haishoku)

### print
https://github.com/willmcgugan/rich

支持emoji表情、table表格、markdown、json等几十种

https://github.com/carpedm20/emoji

### linq
https://github.com/viralogic/py-enumerable

### ebook
https://github.com/kovidgoyal/calibre
Calibre 是一款功能强大的电子书管理软件，支持 Amazon、Apple、Bookeen、Ectaco、Endless Ideas、Google/HTC 与 Hanlin Song 设备及格式。
### pyforest 自动导入需要的包
https://github.com/8080labs/pyforest

### 装饰器(decorators)
- `@lru_cache`来自 functools 模块，该模块包含在标准库中，非常易于使用。
- `@jit`JIT 是即时编译(Just In Time)的缩写。`from numba import jit`
- `@do_twice`此装饰器可用于通过一次调用运行两次函数。该函数由 Python 中的装饰器模块提供，该模块位于标准库中。`from decorators import do_twice`
- `@count_calls`装饰器可用于提供有关函数在软件中使用多少次的信息。这个装饰器也在标准库的装饰器模块中。`from decorators import count_calls`
- `@singleton`
```python
def singleton(cls):
    instances = {}
    def wrapper(*args, \*\*kwargs):
        if cls not in instances:
            instances[cls] = cls(*args, \*\*kwargs)
            return instances[cls]
        return wrapper

@singleton
class cls:
    def func(self):
```
- `@use_unit`此装饰器可用于更改返回结果的表示单位。
```python
def use_unit(unit):
    """Have a function return a Quantity with given unit"""
    use_unit.ureg = pint.UnitRegistry()
    def decorator_use_unit(func):
        @functools.wraps(func)
        def wrapper_use_unit(*args, \*\*kwargs):
            value = func(*args, \*_kwargs)
            return value _ use_unit.ureg(unit)
        return wrapper_use_unit
    return decorator_use_unit

@use_unit("meters per second")
def average_speed(distance, duration):
    return distance / duration
```

### 日期处理
#### Arrow Python时间日期库
其设计灵感主要来源于moment.js。
https://github.com/arrow-py/arrow

> 区别于Apache Arrow；Apache Arrow支持丰富的语言
> 在分布式系统内部，每个系统都有自己的内存格式，大量的 CPU 资源被消耗在序列化和反序列化过程中，并且由于每个项目都有自己的实现，没有一个明确的标准，造成各个系统都在重复着复制、转换工作，这种问题在微服务系统架构出现之后更加明显，Arrow 的出现就是为了解决这一问题。作为一个跨平台的数据层，我们可以使用 Arrow 加快大数据分析项目的运行速度。

#### dateutils
#### pendulum
比Arrow库好用?
https://github.com/sdispater/pendulum

#### Delorean
一个酷炫的日期时间库，类似JavaScript中的moment

### 不会正则表达式的看过来
https://github.com/r1chardj0n3s/parse

### sqlmap
是一款用来检测与利用SQL注入漏洞的免费开源工具，支持所有类型数据库的注入。

### you-get
### wget

### url操作
furl: 简化对url中各部分的操作，例如查询字符串的获取或设置等。
官方地址：https://github.com/gruns/furl

### 任务队列
#### celery
celery：python中最强大的任务队列了，配合Flower可在web界面上实时查看celery的各个任务状态和统计信息

Flower项目地址：https://flower.readthedocs.io/en/latest/

#### huey
huey：一个比较小型的任务队列，依赖于redis或sqlite。

官方文档：https://huey.readthedocs.io/en/latest/

### 定时任务
#### apscheduler
apscheduler：定时任务库，可使用Linux的cron语法来配置任务的启动信息。
官方文档：https://apscheduler.readthedocs.io/en/latest/

### 统计分析
#### Pandas探索性数据分析(Exploratory Data Analysis,EDA)
在使用 pandas 进行数据分析时，进行一定的数据探索性分析（EDA）是必不可少的一个步骤，例如常见统计指标计算、缺失值、重复值统计等。
使用 `df.describe()` 等函数进行探索当然是常见操作，但若要进行更完整、详细的分析缺则略显不足。

- [pandas_profiling 8.1k](https://github.com/pandas-profiling/pandas-profiling)
```
pip install pandas_profiling

from pandas_profiling import ProfileReport
profile = ProfileReport(df), title='Pandas Profiling Report', explorative = True)
profile
```
    - 类型推断：检测数据帧中列的数据类型。
    - 要点：类型，唯一值，缺失值
    - 分位数统计信息，例如最小值，Q1，中位数，Q3，最大值，范围，四分位数范围
    - 描述性统计数据，例如均值，众数，标准偏差，总和，中位数绝对偏差，变异系数，峰度，偏度
    - 最常使用的值
    - 直方图
    - 相关性矩阵
    - 缺失值矩阵，计数，热图和缺失值树状图
    - 文本分析：了解文本数据的类别（大写，空格），脚本（拉丁，西里尔字母）和块（ASCII）


- [sweetviz 1.8k](https://github.com/fbdesignpro/sweetviz)
```
import sweetviz as sv
report = sv.analyze(df)
report.show_html()
```
    1. 目标分析
    - 显示目标值，例如泰坦尼克号数据集中的“幸存”，与其他特征的关系）
    1. 可视化和比较
    - 不同的数据集（例如训练与测试数据）
    - 组内特征（例如男性与女性）
    1. 混合型联想
    - Sweetviz 无缝集成了数值（Pearson 相关）、分类（不确定系数）和分类-数值（相关比）数据类型的关联，为所有数据类型提供最大的信息。
    1. 类型推断
    - 自动检测数字、分类和文本特征，可选择手动覆盖
    1. 概要信息
    - 类型、唯一值、缺失值、重复行、最常见值
    - 数值分析：最小值/最大值/范围、四分位数、平均值、众数、标准偏差、总和、中值绝对偏差、变异系数、峰态、偏度

- [PandasGUI 2.4k](https://github.com/adamerose/pandasgui)
```
from pandasgui import show
# 部署GUI的数据集
gui = show(df)
```

- [Lux 2.9k](https://github.com/lux-org/lux)
```
pip install lux-api

jupyter nbextension install --py luxwidget
jupyter nbextension enable --py luxwidget
```
### 交互UI / 交互式
#### Streamlit / 数据应用
Streamlit是第一个专门针对机器学习和数据科学团队的应用开发框架，它是开发自定义机器学习工具的最快的方法，你可以认为它的目标是取代Flask在机器学习项目中的地位，可以帮助机器学习工程师快速开发用户交互工具。
[github](https://github.com/streamlit/streamlit)
[Streamlit docs](https://docs.streamlit.io/)

#### PyWebIO
[PyWebIO](https://github.com/pywebio/PyWebIO)

#### 高维数据
https://github.com/facebookresearch/hiplot

### 数据可视化工具

#### 开源的可视化数据管道构建工具：Orchest

#### 缺失值可视化
https://github.com/ResidentMario/missingno
#### Kepler.gl
[Kepler.gl](https://kepler.gl/)相信很多人都听说过，作为Uber几年前开源的交互式地理信息可视化工具，kepler.gl依托WebGL强大的图形渲染能力，可以在浏览器端以多种形式轻松展示大规模数据集。
https://github.com/keplergl/kepler.gl

##### Geo Data Viewer
https://github.com/RandomFractals/geo-data-viewer


#### python的matplotlib
- [D3渲染Matplotlib图形](https://github.com/mpld3/mpld3) 新版的matplotlib自带了mpld3


 • Matplotlib：标杆，必须知道
 • Seaborn：更漂亮、更好用的Matplotlib
 • Mpld3：Matplotlib + 交互式(D3实现)
 • Bokeh：更漂亮 + Matplotlib + 交互式
 • Altair：声明式统计数据可视化
 • Folium：交互式地图可视化

#### 高维数据的可视化分析

[dimensions visualization](https://github.com/openjw/penter/scikit-learn/dimensions_visualization.ipynb)

[AutoViz](https://github.com/AutoViML/AutoViz)（自动完成数据可视化）

#### R语言的ggplot2
#### pandas_alive
Pandas_Alive，它以 matplotlib 绘图为后端，不仅可以创建出令人惊叹的动画可视化，而且使用方法非常简单。
https://github.com/JackMcKew/pandas_alive

#### EDA
探索性数据分析（Exploratory Data Analysis，简称EDA）

Pandas Profiling、Sweetviz和PandasGUI都很不错，旨在简化我们的EDA处理。在不同的工作流程中，每个都有自己的优势和适用性，三个工具具体优势如下：
[Pandas Profiling](https://github.com/pandas-profiling/pandas-profiling) 适用于快速生成单个变量的分析。
[Sweetviz](https://github.com/fbdesignpro/sweetviz) 适用于数据集之间和目标变量之间的分析。
[PandasGUI](https://github.com/adamerose/pandasgui)适用于具有手动拖放功能的深度分析。

[AutoViz](https://pypi.org/project/autoviz/)

还有其他有趣的 AutoEDA 库，如 Dora、D-Tale 和 DataPrep

#### Altair

## Python神器

### 性能分析/代码分析器
cProfile

### 收集
[轻量级 Python 流水线工具Mara Pipelines](https://github.com/mara/mara-pipelines)

### 为Python应用程序创建调用图可视化
https://github.com/gak/pycallgraph
https://pycallgraph.readthedocs.io/en/develop/examples/regexp_ungrouped.html#regexp-ungrouped-example

### 可视化排序算法
https://github.com/LucasPilla/Sorting-Algorithms-Visualizer
### 可视化在线编写运行Python的神器：PythonTutor
有点像图解python运行过程
http://www.pythontutor.com/

### 可视化Python调试工具 - Birdseye
https://mp.weixin.qq.com/s/4aCfBq1xA_ctrtHXnxcYlA
### 优秀的Debug神器---pysnooper
有点像日志输出python运行过程
https://github.com/cool-RR/PySnooper 13.8k
```
https://github.com/cool-RR/PySnooper/blob/master/ADVANCED_USAGE.md
import pysnooper
#@pysnooper.snoop()
@pysnooper.snoop('file.log')
@pysnooper.snoop(watch=('foo.bar', 'self.x["whatever"]')) 查看变量
@pysnooper.snoop(depth=2)
```
### heartrate 程序执行实时可视化
Python程序执行的简单实时可视化。
https://github.com/alexmojaki/heartrate
代码调用高亮依赖于[executing](https://github.com/alexmojaki/executing) 库

### VizTracer 工具可以可视化并跟踪 Python 代码
https://github.com/gaogaotiantian/viztracer

VizTracer 是一个这样的工具，它通过跟踪和可视化 Python 代码的执行过程，来帮助你对代码的理解。无需对源代码进行任何更改，VizTracer 即可记录函数的入口 / 出口，函数参数 / 返回值以及任意变量，然后通过 [Trace-Viewer](http://google.github.io/trace-viewer/) 使用直观的谷歌前端界面来显示数据。

[Understand your Python code with this open source visualization tool](https://opensource.com/article/20/11/python-code-viztracer)

### 可视化调试工具: Cyberbrain
https://github.com/laike9m/Cyberbrain

重新定义python的debug
可视化
### pyinstrument
堆栈分析器
https://github.com/joerick/pyinstrument

Python 代码性能分析库，优化 Python 代码的工具。支持 Python 3.7+ 能够分析异步代码，仅需一条命令即可显示具体到函数的耗时，快速指出影响代码性能的地方，帮助提高代码性能让你的代码快人一步。

### Debug Visualizer
https://github.com/hediet/vscode-debug-visualizer

vs code插件，支持多种语言
- JavaScript/TypeScript/
- Dart/Flutter
- Go
- Python 
- C#
- PHP 
- Java 
- C++
- Swift 
- Rust 

## jupyter
### lux
https://github.com/lux-org/lux

### PyXLL-Jupyter
[将Jupyter Notebook嵌入到Excel中](https://github.com/pyxll/pyxll-jupyter)

### mitosheet
Mito是Jupyter notebook的一个插件，作用是编辑电子表格，并在编辑表格（带格式转换功能）时，可以生成相对应的Python代码。

```
python -m pip install mitoinstaller
python -m mitoinstaller install
python -m jupyter lab
```
等价
```
pip install mitosheet
jupyter labextension install @jupyter-widgets/jupyterlab-manager@2
jupyter lab
```



```
import mitosheet
mitosheet.sheet()
```

### Latex 公式/python代码输出数学公式
https://github.com/connorferster/handcalcs

## 流程图
https://github.com/mingrammer/diagrams

## 翻译
https://github.com/UlionTse/translators


## 文档
https://github.com/scanny/python-pptx

https://github.com/python-openxml/python-docx

https://foss.heptapod.net/openpyxl/openpyxl
https://pypi.org/project/openpyxl/

[将Jupyter Notebook嵌入到Excel中 - pyxll](https://github.com/pyxll/pyxll-jupyter)
[在web中使用Python编辑excel - gridstudio](https://github.com/ricklamers/gridstudio)
[基于python开发的excel插件 - sqlcelpy(数据分析) ](https://sqlcel.com/)
[Excel 中调用 Python 脚本 - xlwings](https://github.com/xlwings/xlwings)

数据管理的库
[Tablib](https://github.com/jazzband/tablib) 是一个与表格格式数据有关的Python库，允许导入、导出、管理表格格式数据。
Output formats supported:
- Excel (Sets + Books)
- JSON (Sets + Books)
- YAML (Sets + Books)
- Pandas DataFrames (Sets)
- HTML (Sets)
- Jira (Sets)
- TSV (Sets)
- ODS (Sets)
- CSV (Sets)
- DBF (Sets)

excel相关：
xlrd：读取excel文档
xlwt：写excel文档
pyexcel：读写excel文档（只能xlsx格式）

## Python 
### 学习
这个有趣的项目意在收集 Python 中那些难以理解和反人类直觉的例子以及鲜为人知的功能特性, 并尝试讨论这些现象背后真正的原理!
https://github.com/satwikkansal/wtfpython

https://github.com/jerry-git/learn-python3
https://github.com/trekhleb/learn-python
https://github.com/joaoventura/full-speed-python
https://github.com/rasbt/python_reference/
https://github.com/zhiwehu/Python-programming-exercises
https://github.com/MTrajK/coding-problems/

### 算法
https://github.com/TheAlgorithms/Python/

### 错误
知道了性能瓶颈，那就要解决深层次的原因，或许是逻辑上的问题，或许是有异常代码。
PrettyErrors只做一件事并且做得很好。
https://github.com/onelivesleft/PrettyErrors


### CPU和内存探查器
Scalene是用于Python脚本的CPU和内存探查器，能够正确处理多线程代码并区分运行Python和本机代码所花费的时间。
https://github.com/emeryberger/scalene

### 其它
代码画图
https://github.com/mingrammer/diagrams

## 音频处理
### klio
https://github.com/spotify/klio

## 图片和视频
### DeepFaceLab
https://github.com/iperov/DeepFaceLab
DeepFaceLab 是本文中 GitHub 上最有趣的 Python 项目之一。
DeepFaceLab 是一种工具，可以创建深层假图像和视频，它允许你做很多有趣的事情，如改变、取消年龄和交换脸。为了让事情更有说服力，你甚至可以改变他们的语言，尽管这需要精通视频编辑软件。

### ORC
- https://pypi.org/project/muggle-ocr
- https://gitee.com/raoyutian/paddle-ocrsharp
- https://gitee.com/paddlepaddle/PaddleOCR 
- https://github.com/PaddlePaddle/PaddleOCR

## 机器学习
### 机器学习UI框架Streamlit - 好东西

https://github.com/streamlit/streamlit 11.6k

Streamlit 是 Python 编写的开源应用框架，数据科学家用其来构建好看的数据可视化应用。Streamlit 专注于快速原型设计，并且支持各种不同的可视化库(包括 Plotly和Bokeh)，因此在Dash等竞品中脱颖而出。
对于需要在实验周期中快速展示的数据科学家来说，Streamlit 是一个可靠的选择。我们在一些项目中使用它，并且只需要花费很少的工作量就能把多个交互式可视化放在一起。


## 其它整理
### Manim
https://github.com/3b1b/manim

Manim 代表数学动画引擎。这个项目背后的理念是让人们更容易地将有趣和直观的动画与数学教材中的图形和图表相结合，从而打破学习数学必须枯燥乏味的刻板印象。

Grant 经营着一个名为3Brown1Blue（国内俗称：3黄1绿）的YouTube频道，在那里他使用Manim库来创建和控制这些动画，向观众教授更高的数学。使用 manim，你还可以创建动画视频，并精确控制用于图表和插图的动画。

Youtube链接: https://www.youtube.com/channel/UCYO_jab_esuFRV4b17AJtAw

B站链接：https://space.bilibili.com/88461692


### Airflow 
工作流管理工具。
https://github.com/apache/flow

### google-images-download 谷歌图片下载

GitHub 链接：https://github.com/hardikvasa/google-images-download

Hardik Vasa 的脚本允许我们一次性从 Google 上下载数百张图片到本地计算机。此工具的工作方式是安装库、使用命令、将所需的关键字作为参数，以及让该工具发挥其神奇的作用。本质上是在google images 索引中搜索带有指定关键字的图片，找到后就进行下载。

### XSStrike

GitHub 链接：https://github.com/s0md3v/XSStrike

跨站点脚本（又名 XSS）是一个漏洞，对网站来说可能非常烦人和有害。通过从客户端注入恶意代码，攻击者可以对网站和数据造成无法控制的损害。
s0md3v 的 XSStrike 本质上是一个 XSS 检测套件，它本身是独一无二的。

开发人员声称，他的工具不是简单地测试随机有效负载，而是分析网站并生成具有工作效果的专门工程有效负载。此工具的一些各种功能包括：

- 上下文语境分析
- 强大的模糊引擎
- 支持多线程分析
- 支持从文件中消除有效负载
- 定制的 HTML 和 JavaScript 解析器
- 扫描任何过时的 Javascript 库


### Xonsh
Xonsh shell 
https://github.com/xonsh/xonsh

### Rebound

GitHub 链接： https://github.com/shobrook/rebound

编译器错误非常令人厌烦，唯一的解决方案是直接进行堆栈溢出或阅读文档。Jonathan Shobrook和他的著名工具 Rebound，已经找到了一种方法，可以让我们的工作变得更容易，同时还可以处理那些讨厌的编译器错误。

Rebound的工作方式是，使用该工具运行文件，它会检查文件中存在的任何编译器错误，并获取它能找到的任何相关的堆栈溢出线程。

Rebound的能力，加载线程在终端和浏览器中可以是一根救命稻草，不仅你是新手，还是老程序员，都可以节省大量的时间进行无休止地寻找答案。目前，Rebound 仅支持 Python、Node.js、Ruby、Golang 和 Java。