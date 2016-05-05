# Google C++ 单元测试框架（Gtest）

----------

## 单元测试
单元测试作为软件开发过程中最低级别的测试环节，通常由专门人员编写，目的值隔离程序部件，并证明单个部件满足预期功能。在静态程序分析、代码检视之后进行单元测试，可有效及时发现开发过程早起遇到的各类问题，一般的，一个好的测试应包含以下特点：

* 独立
* 有效的组织架构，清晰的命名
* 可移植、可复用
* 当用例失败时，提供尽可能多的有效信息

## Google C++ 单元测试框架
Google C++单元测试框架（简称Gtest），可应用于多个平台上（Linux、Mac OS X、Windows、Cygwin和Symbian），它提供了丰富的断言、致命和非致命失败判断，能进行值参数化测试、类型参数化测试、“死亡测试”。Gtest是一个开源的项目。

使用Gtest的步骤如下：

* 下载Gtest
下载链接为：[https://code.google.com/p/googletest/downloads/list](https://code.google.com/p/googletest/downloads/list "https://code.google.com/p/googletest/downloads/list")

* 认识文件夹
![](http://i.imgur.com/brG1Ldx.png)

由于GTEST提供了对于多个不同平台的支持，文件夹中包含了各个平台所用的文件夹，如msvc文件夹是用在微软Visual Studio中，xcode文件夹是用于Mac Xcode，codegrear文件夹是用于Borland C++ Builder，make文件夹用于linux。

* 清楚不需要的文件
上一步已经说明，很多文件夹的存在是为了支持不同平台，在此处以linux下Gtest安装和使用为例，删除不需要的文件后情况如下：
![](http://i.imgur.com/uISRKL7.png)

其实打开make文件夹，发现里面只有一个Makefile文件。查看Makefile文件内容，得知这是系统给出的编译samples文件夹中的第一个sample的命令。但是打开sample文件夹，又看到里面一大坨源文件。在本入门教程中，我们先不考虑那些复杂的例子。因此，打开samples文件夹，开始删文件，删到只剩下如图所示的三个文件：sample1.cc、sample1.h、sample1_unittest.cc




