# MAP55614-C-Programming-2021
## Assignment-1 <a name="Assignment-1"></a>
For this assignment you will write some functionality for a class that we will call Gaussian. 
The bones of the class are provided along with a main function in the file assignment1.cc. 
You will write some member function definitions for the class, and also some non-member functions that provide the same functionality. 
The purpose of this is so that you can see both approaches. We will discuss the merits later.

为了这个作业，你将为我们称之为高斯的类编写一些功能。
类的框架已经提供，以及文件assignment1.cc中的一个主函数。
你将为类编写一些成员函数定义，以及提供相同功能的一些非成员函数。
其目的是让你能看到两种方法。稍后我们将讨论这些方法的优点。

The Gaussian distribution, $N (μ, σ^2)$, has probability density function

高斯分布, $N(μ, σ^2)$, 有概率密度函数

$$\phi(x) = \frac{1}{\displaystyle \sigma \sqrt{2\pi}} e^{\displaystyle -\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$$

You will write functions which calculate the $φ(x)$ and also which approximate
the Cumulative Distribution Function (CDF), $Φ(x) = \int_{-\infty}^{x} φ(t)dt$, using numerical integration. 
你将编写计算$\phi(x)$的函数，以及使用数值积分近似计算累积分布函数（CDF），

You can compare your answer to a polynomial approximation for same. The code is included for the polynomial approximation and, for reference, is based off the <a href="http://finmod.co.za/Better%20Approximations%20To%20Cumulative%20Normal%20Functions.pdf.
">document</a>

你可以将你的答案与同样的多项式近似进行比较。多项式近似的代码已经包括在内，作为参考，它是基于<a href="http://finmod.co.za/Better%20Approximations%20To%20Cumulative%20Normal%20Functions.pdf.
">文档</a>

You will also use the identity that
你还将使用恒等式

$$\Phi(x) = \frac{1}{2} + \frac{1}{2}\text{erf}\left(\frac{x}{\sqrt{2}}\right)$$

and the inbuilt standard library complimentary error function, std::erfc, as an alternate way to calculate the same thing.
The main function is provided. You can write your own equivalent one, or else comment out bits of this one so that you can check that your code compiles as you are writing the individual functions. But when you submit the assignment, it should ideally be running with the provided main function.

和内置的标准库互补误差函数，std::erfc，作为另一种计算相同事物的方法。
主函数已经提供。你可以编写自己的等效函数，或者注释掉这个函数的一些部分，以便在编写各个函数时检查你的代码是否编译。但是当你提交作业时，理想情况下应该使用提供的主函数运行。

## Note Comments <a name="Comments"></a>

<p>在这个作业中，注释将占总分的20%。类似于5613课程，你应该尝试使用一些Doxygen注释。你可以在这里查看一些基础知识<a href = "http://doxygen.nl/manual/docblocks.html"> doxygen </a>
在包含高斯分布的代码中有一个例子：Gaussian::cdf_poly。例如，你可以包括以下指令
<ul>
<li><code>\brief</code></li>
<li><code>\param</code></li>
<li><code>\return</code></li>
</ul>
</p>

<p>在你编写的函数之前，应该使用Doxygen注释。Doxygen指令可以用 "@" 来标记，比如 @brief 等。在代码的适当位置使用其他注释。你应该至少在每个函数之前都有一个描述，向用户解释它的功能。</p>

# Q1-Makefile (5%)

Write a very simple Makefile to take care of your assignment. For anyone who might join the class late and who did not take 5613, see a quick example at <a href = "https://www.gnu.org/software/make/manual/html_node/Simple-Makefile.html">GNU Make</a>. 
Your makes will have two targets:
<ul>
    <li>1. assignment1</li> 
    <li>2. clean</li>
</ul>

编写一个非常简单的 Makefile 来处理你的作业。对于那些可能迟到加入课程并且没有上过 5613 的人来说，请在<a href = "https://www.gnu.org/software/make/manual/html_node/Simple-Makefile.html">GNU Make</a>手册 中看一个快速示例。你的 Makefile 将有两个目标：
<ul>
    <li>1. assignment1</li> 
    <li>2. clean</li>
</ul>

<code>make clean</code> 
should just delete the executable. Mark clean as a .PHONY target.
For this assignment, set some variables at the start of the Makefile and use these in your compilation commands. You can define and set them up however you like but I would suggest that you have at least something like

<code>make clean</code> 应该只删除可执行文件。将 clean 标记为 .PHONY 目标。
对于这个作业，在 Makefile 的开始部分设置一些变量，并在编译命令中使用这些变量。你可以随意定义和设置它们，但我建议你至少应该像这样设置：

<pre>
CC := g++
CFLAGS := −W−Wall −std=c++17
</pre>

You can <a href = "https://www.gnu.org/software/make/manual/html_node/Reference.html">see</a> for information about using variables in your makefile. If there is a location
in your Makefile where you would otherwise have the command 
<code>g++ -W -Wall-c file.c</code> 
then you would just replace it by <code>$(CC) $(CFLAGS) -c file.c</code>
etc.


# Q2-Inline functions (20%)
The first five functions should all be written inside the class definition.

前五个函数都应该在类定义内部编写。


## (A) Constructors (10)

Write the default constructor for class Gaussian. The bones of the class are provided. The class contains two private members we can refer to below as $μ$, $σ$.

<pre>
Gaussian ()
</pre>


<p>This constructor should use a member initialisation list to initialise μ with value 0, σ with value 1. Include a statement in the constructor which causes the sentence “Constructing default with mean 0.0, stdev 1.0” to be printed when the constructor is called 1.
Next, write an overloaded constructor
</p>

## (B) Return $z$ value (5)

## (C) Accessor Functions (5)

# Q3-Copy constructor/assignment operator (10%)

# Q4-Other class member functions (20%)

# Q5-Non-member (free) functions (20%)

# Q6-Putting it all together (5%)

# Q7-Written Questions (20%)