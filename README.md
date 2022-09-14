# 如何用PyCharm建立一个新的工程
## 阅读本文后, 本文你将学会
- [x] 初步认识PyCharm
- [x] 初步理解PyCharm的环境
- [x] 使用PyCharm建立新的工程
- [x] 理解什么是interpreter, 什么是terminal, 什么是text editor

### 什么是PyCharm
* PyCharm是一种文本编辑器(IDE), 在指定Python的环境下能够运行用Python语法编写的特定文本。PyCharm中的编译器不仅能够运行以`.py`文件为结尾的文件, 还支持其他语言的编译, 包括但不仅限于`.html`, `.sql`, `.scheme`, `.md`等等。(编译器是指将文件进行编译, 链接, 处理的工具)也就是说, 当我们建立新的工程后, 在工程中这些文件都是可以被文本编辑器中的编译器(Compilor)运行或理解的。总之, PyCharm是一款功能强大的IDE, 能够满足日常对Python文件的编辑需要。

### 什么是Python的环境(Environment)
* 如下图所示, 这是在我的电脑中的Python的地址。当我们调用Python进行编译时, 实际上也是在利用`python.exe`这个可执行文件进行文本的解释或运行。\
[![Python环境地址](https://i.postimg.cc/HnSz36d6/20220914234001.jpg)](https://postimg.cc/wRmDjctN)
如下图所示，是`python.exe`可执行文件。\
[![python.exe](https://i.postimg.cc/sgCmmGrd/20220914234504.jpg)](https://postimg.cc/3d92JRNn)
按简单的方式理解, Python其实也是一个普通的可执行应用程序。那么, 就像一般的应用程序, python也会有不同的版本和更新。**我们所说的Python的环境就是Python的不同的版本。通过设置不同的环境， 我们可以在不同版本的Python下运行`.py`文件。**

### 如何建立一个新的工程(Project)
* 下面我们建立一个新的工程。
如下图所示, 当我们初始化进入PyCharm后, 会进入如下所示的界面。在右侧第一行, 我们选择`New Project`一栏, 点击。
[![建立一个工程](https://i.postimg.cc/qvM7KQ5N/20220914235345.jpg)](https://postimg.cc/8j9DQdDG)
之后我们将进入如下图所示的界面。点击`Python Interpreter 3.9 Default`可以展开。如果你的电脑已经安装了Python的环境, PyCharm将自动识别出来。在第一栏， `location`中, 这是PyCharm给我们的工程新建的文件路径。可以按照你喜欢的配置更改工程名称, 下面我将把文件夹命名为`pycharm_test`(文件夹一般使用小写, 空格用`_`替代)。
[![初始配置](https://i.postimg.cc/Gt2DqrMy/20220914235136.jpg)](https://postimg.cc/JDfthwCr)
我们继续看下面这一栏, PyCharm自动帮我们选好了`Previously configured interpreter`, 这将会是我们的解释器的环境(Python的版本)可以看到, 在Interpreter那一行, 他的文件地址就是我们前文所说的电脑中`python.exe`的应用程序的地址。也就是说, 如果我们下载了不同的Python版本, 并存放在电脑不同的文件地址中, 我们就可以有不同的Python环境。这也就是上一栏`New environment using`的含义, 使用不同于初始(Default)版本的Python进行编译。
[![环境(environment)与解释器(interpreter)](https://i.postimg.cc/wv3bdZFY/20220915000309.jpg)](https://postimg.cc/MM2Y7sh9)
* 在底层, 我们可以看见一栏
`- [ ] Create a main.py welcome script`
如果我们选择这一选项, 那么在我们建立新的工程(Project)后, 文件夹中会自动新建一个`main.py`的文件, 里面含有欢迎我们使用PyCharm的脚本内容, 实际意义不大。这里跳过这一选项。
* 点击`create`建立新的工程(Project)
* 这是我们便进入了一个全新的界面!
[![新工程界面](https://i.postimg.cc/J4hg3yjz/20220915001512.jpg)](https://postimg.cc/grfNm2MC) 
下面我将介绍一些功能与按钮。
在右下角, 我们可以看见`Python 3.9(Default)`的字样, 这就是我们**这个工程**的解释器。
在左下角, 我们可以看见`Terminal`的字样, 这就是我们在PyCharm下的终端, 可以执行类Linux的命令, 在此我们只需要熟悉一个, 当在终端打入`python`命令后, 终端会自动进入我们**这个工程**的解释器环境。可以在此Python环境下执行我们符合Python语法的命令。这就是解释器的作用。
* 熟悉了一些PyCharm界面以后, 我们在我们的工程下建立一个新的文件吧!
如下图所示, 右键pycharm_test文件夹, 将光标移至图片处, 我们可以建立一个`.py`的文件。
[![建立一个.py文件](https://i.postimg.cc/hG9zCtVX/20220915002336.jpg)](https://postimg.cc/gw22jdSp)
我们将文件命名为`test.py`
[![20220915002703.jpg](https://i.postimg.cc/DftcY8Xg/20220915002703.jpg)](https://postimg.cc/MXmRnZtM)
好了! 我们现在就自己建立了一个`.py`文件了!
* 打出自己的第一行Python代码
将以下代码复制到`test.py`文件中\
```
def main():
    print("Hello, Python!")


if __name__ == "__main__":
    main()
```\
现在, 如何运行这个文件呢?
这就是终端解释器(terminal interpreter)与编辑器(text editor)的区别了。
### 什么是终端(terminal), 解释器(interpreter)与编辑器(text editor)
* 解释器是在解释并运行我们的一行指令, 而编辑器是可以运行整个文件的。当我们的文件有输出时, 是可以在输出面板看到我们的输出的。这时就需要我们在PyCharm中配置运行文件的路径了, 也就是告诉PyCharm要运行哪个路径下的`.py`文件。
* 配置运行环境。
* 点击左侧`Add new...`可以配置新的运行环境。刚刚我们所说的解释器环境是指解释器进行解释的Python环境(environment), 也就是Python的版本。同理，运行环境也可以配置运行的Python环境(environment)。
[![配置运行环境](https://i.postimg.cc/QtBfHzPg/20220915003658.jpg)](https://postimg.cc/8JSRYZTs)
* 我们将运行环境命名为`pycharm_test`
* 建立好后应该如下图所示。
[![建立运行环境](https://i.postimg.cc/6qh04N9P/20220915004405.jpg)](https://postimg.cc/D48sRH4Q)
* 选择文件路径
在右侧第一行`Script Path`
什么是`Script`呢? 
`Script`翻译为脚本, 也就是我们所写的代码。我们选定`test.py`文件的路径, 运行环境便会在这个文件路径下运行`python.exe`, 也就是执行我们的`test.py`文件。
[![选择文件路径](https://i.postimg.cc/YCywL50j/20220915004806.jpg)](https://postimg.cc/ZW3Q1Drh)
* 选择此文件路径, 点击`OK`
* 再次点击`OK`
* 在下图右上角, 我们可以看见一个绿色的[![运行标志](https://i.postimg.cc/1zfVp1Kd/20220915005138.jpg)](https://postimg.cc/WDc4vKCm), 点击它, 便可以运行文件了!
* 我们可以看见我们运行成功啦! 在下方, 如图所示!
[![运行成功](https://i.postimg.cc/pLB3KgdK/20220915005519.jpg)](https://postimg.cc/Xrp2b1dv)
### 总结
我们学习了什么是PyCharm, 如何建立工程(Project), 解释器(interpreter), 终端(terminal)以及编辑器(text editor)是什么, 运行环境和解释器环境有什么不同。现在, 发挥自己的创造力, 尽情编写代码吧!
> Let the Python Magic Begin!\
[![better-debugging.png](https://i.postimg.cc/gj9SZPfy/better-debugging.png)](https://postimg.cc/k6cF0LMD)
