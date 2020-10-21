# Hedy 海迪
Hedy（海迪）是一门循序渐进的编程语言，旨在按照由易到难的方式教授编程和Python。第一级目标是打印文本和要求输入。这个级别是为了向学习者介绍编程语言的概念以及运行环境。从这一级目标开始，Hedy（海迪）逐级建立了更复杂的语法和概念。

最新版本的Hedy（海迪）可以在以下网站找到，[hedy-beta.herokuapp.com](https://hedy-beta.herokuapp.com).


设计原则及目标
==============================

设计原则
------------

    Hedy（海迪）的总体目标是在类似Python的语言中不断增加语法的复杂性，
直到初学者掌握Python。
    为了达到这个目标，Hedy（海迪）遵循以下设计原则：

1.  **设计原则1. 新概念至少以不同的形式出现三次:** 

    写作教育的研究表明，最好在很长一段时间内以不同形式引入一个概念。此外，
有研究表明，一个单词需要阅读7遍才能被储存在长时记忆中。

2.  **设计原则2. 首次引入一个新概念时要尽可能使用最简单的形式:**

    已有研究表明，语法可能会使初学者感到困惑。因此，较低层次目标里面
尽可能不涉及语法以降低认知负荷。

3.  **设计原则3. 每次只改变一个概念的一个方面e:** 

    Shneiderman提出螺旋式教学法[the spiral approach Shneiderman]
(https://www.sciencedirect.com/science/article/pii/0360131577900082)，
他主张在编程教学中采取“小步走”的策略，我们在Hedy（海迪）目标设计过程
中也采取这种策略。这样我们就可以让学习者集中全部的注意力去学习新的语法元素。

4.  **设计原则4. 尽可能到最后再学习添加括号和冒号等语法元素:** 
    
    计算机科学教育领域的已有研究表明，像双等于号（==）和冒号（：）这样的
运算符对初学者来说特别难。在一项针对荷兰高中生的研究中[study](https://www.felienne.com/archives/5947)，
我们发现造成这些困难的原因可能是他们的读码方式。
    有关自然语言习得的研究也表明，小括号和冒号是学习者通常最后学习的标点符号。
所以如果必须在冒号，小括号和其他元素比如缩进三者之间进行选择，应该选择先学习缩进。

5.  **设计原则5. 学习一个概念的不同形式尽可能和学习其他概念的不同形式交替进行:** 
    
     我们知道，间隔重复是一种很好的记忆方式，而学习标点符号需要花费时间，
 所以在语法变化之前，我们要尽可能给学生提供更多的机会来学习概念。


6.  **设计原则6. 当（学生）达到每个层次的目标的时候都有可能编写出简单而有意义的程序:**
    
    对所有学习者来说，参与有意义的活动是很重要的。我们在教授高中生（甚
至是大学计算机专业的学生）的经验是，学习语法并不总是被视为一种有用的活
动。学生既体验到计算机很聪明，例如能够在几秒钟内计算出1,910和5,671乘积，
同时也认识到计算机（有时也很笨）甚至不能独立地添加一个漏掉的冒号。我们
预计当初始语法简单，让初学者可以应用它们编写一个有趣而有意义的程序时，
他们以后会有更多的动力去学习语法的细节。

Levels 各个级别的具体目标
------

    目前，Hedy（海迪）编程课由 13 个不同层次的具体目标组成。这些目标
大致遵循 “Python课堂”系列编程课程("Python in the classroom")(http://pythonindeklas.nl/)，
因此这些现有课程可以选择用编程语言Hedy（海迪）代替Python。

### 第1级目标：打印和输入

    在第1级，学生首先可以用“print”打印文本。为此，除了保留字 [`print`]
和任意文本之外，不需要任何语法元素。此外，学生可以使用保留字 [`ask`]要求
用户输入。这里我们决定使用[`ask`] 而不是 [`input`] 因为它更符合保留字在
代码中的作用，与它做什么无关。 
    用户输入可以用 [`echo`]来重复，所以可以创建非常简单的程序，在程序中
询问用户的名字或最喜欢的动物，实现设计原则6。

### 第2级目标：用is来定义变量

    在第2级，我们在语法中引入了变量。用 [`is`] 而不是等号来定义变量，以实
现设计原则3和4。我们还引入了列表操作，增加了创建列表和检索列表，包括用
[`at`]从列表中检索元素。添加列表，尤其是从一个列表中随机选择元素的选项
有助于创建更多有趣的程序，比如猜谜游戏、带有随机元素的故事（
这是“Python课堂”系列编程课程）(http://pythonindeklas.nl/)的一个作业），
或者一个可以定制的骰子。

### 第3级目标：引号和变量类型

    在第3级中引入了第一个语法要素：使用引号来区分字符串和文本。在教授初学
者的过程中，我们已经看到这种区分在很长一段时间内都会让人感到困惑，因此尽
早提出这种区分可能有助于人们注意计算机所需变量类型信息。因此，这一层次是
解释语法和解释编程概念的有趣结合，它强调了它们之间的相互依赖性。
使用[`is`]的变量语法保持不变，这意味着学习者现在既可以使用
[`number is 12`] 也可以使用[`name is Hedy`]。


### 第4级目标：使用if 和else条件语句的选择结构

    在第4级目标，引入了使用if语句的选择结构，但语法是 "平的"，即放在同一
行，更类似于常规语法:\
[`if name is print `]\
    第4级目标也包括Else语句，也是放在同一行，使用保留字
[`else`]:\
[`if name is print else print `]

### 第5级目标：用repeat x times的循环结构

    已有研究发现，对于母语为非英语的Python初学者来说保留字 [`for`] 是一个
令人困惑的重复词，尤其是它听起来像单词‘four’ [@hermans_code_2018]。因此，
遵循设计原则2，对于第一个最简单的形式，我们选择使用 [@stefik_quorum_2017] 
语法 [`repeat x times`] 语句。 在这个初始形式中，在这个初始形式中，像if语
句一样语法是放在同一行:\
[`repeat 5 times print `]

### 第6级目标：计算

*注：这一级目标原来是第4级目标，现在提升到第6级。可以根据目前学生们测试的经
验，再移到其他地方。*
    在第4级目标，学生学习变量之间的计算，因此引入了加法、乘法、减法和除法。
虽然这似乎是一个简单的步骤，但我们的经验告诉我们，使用 [`*`] 来表示乘法，
而不是 $\times$，倍数，以及对于非美国学生来说使用句号而不是逗号作为的小
数分隔符，这些困难形成了一条陡峭的学习曲线，即要求学生在短时间内掌握大量
的知识，因此这应该被视为一个单独的学习目标。

### 第7级目标：代码块

    在第 6 级目标之后，显然需要 "继续前进"，因为一个循环语句(以及 if条件语
句) 只能由一行组成，这限制了用户编写程序的可能性。我们假设这种限制会成为学习
者的动力，而不是“不得不学习”Python区块链，他们的动力来自于创建更大和更有趣的
程序的未来期望(设计原则6)。依据原则3，循环语句的语法保持不变，所以新的形式是:\

[`repeat 5 times`]\
[`print `]\
[`print `]\

### 第8级目标：For语法

    一旦代码块充分自动化，学习者将看到一个更像Python形式的for循环语句，即:
[`for i in range 0 to 5`].
这样就可以访问循环变量 [`i`] ，这就可以实现更有趣的程序，比如数到10。依据设
计原则3，一点一点的改变，为了做到这一点（遵循原则4），括号和冒号被推迟到后面
更高的目标层次里，但在第7级目标学到的缩进仍然存在。

### Level 9: 第9级目标：学习冒号

    为了向完整的Python迈进，学习者需要在循环语句和条件语句中使用冒号来标记一
个代码块的开始。因为代码块是已知的，我们可以教学习者在每个缩进前使用冒号，并
让他们进行大量的练习。

### 第10级：循环结构的嵌套和选择结构的嵌套

    为了让概念之间有足够的交替（设计原则5），我们推迟了小括号的引入，而专注于
更多的概念补充：代码块的嵌套。我们知道缩进对学生来说是一个很难学习的概念，所以
需要有自己的目标层次（依据设计原则3）。

### 第11级目标：添加小括号

    第11级目标在 [`print`], [`range`] 和 [`input`] 中增加了小括号。依据设
计原则4，这些都在尽可能晚地时候添加的。

### 第12级：添加中括号

    在第12级目标中，学习者第一次遇到了不同类型的括号，为了访问列表而引入了中括
号，依据设计原则2，目前都是使用保留字 [`at`]来完成。

### 第13级目标：is变成了=和==

    在最高一级目标里 [`is`] 被替换为用于赋值的等于号 [`=`] 或者用于判断是否相
等的双等于号 [`==`]，这样Hedy （海迪）就成为了 Python 的一个子集。

想要帮助改进Hedy吗？
------------

请在这里查看我们如何使用您的帮助: [CONTRIBUTING.md](CONTRIBUTING.md).
