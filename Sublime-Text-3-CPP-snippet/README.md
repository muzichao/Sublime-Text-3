#### Sublime Text 3 CPP snippet

在sublime text中可以使用snippet功能自定义代码段来提高代码效率。

#### 创建新的代码段

点击菜单栏的`Tools（工具）`菜单，然后点击`New Snippet（新的代码段）`，之后会在新的tab页创建一个代码段模板，如下所示：

    <snippet>
        <content><![CDATA[
    Hello, ${1:this} is a ${2:snippet}.
    ]]></content>
        <!-- Optional: Set a tabTrigger to define how to trigger the snippet -->
        <!-- <tabTrigger>hello</tabTrigger> -->
        <!-- Optional: Set a scope to limit where the snippet will trigger -->
        <!-- <scope>source.python</scope> -->
    </snippet>

#### 语法说明

+ <content><![CDATA[...]]></content> ：省略号处为想要定义的代码段。如：想要定义`using namespace std;`代码段，只需写为：<content><![CDATA[using namespace std;]]></content>

+ \${1:this} 和 \${2:snippet} 是占位符。在插入代码片段后，单词 this 被选中，如果键入内容，this 将会被替换掉，接着按下 Tab 键，将会选中单词 snippet，如果键入内容，snippet 将会被替换掉。

+ <tabTrigger>hello</tabTrigger> 默认被注释掉了。这个选项的意思是说：如果在某个文档里输入了单词 hello ，然后按下 Tab 键，接着 hello 就会被替换为我们自定义的代码段。此处的hello可以改为我们想要设置的字符串。

+ <scope>source.python</scope> 默认也被注释掉了。这个选项的意思是说：此代码段只在python文件中起作用。

<<<<<<< HEAD

当然，还可以定义为其他语言。

> c++：source.cs
> TeX: text.tex
> Matlab: source.matlab
> Latex: text.tex.latex
> Objective-C: source.objc
> Objective-C++: source.objc++
> YAML: source.yaml
> XML: text.xml
> SQL: source.sql
> C#: source.cs
> Java: source.java
> Javascript: source.js
> Markdown: text.html.markdown
> Python: source.python
=======
当然，还可以定义为其他语言。

> c++：source.cs
    
> TeX: text.tex

> Matlab: source.matlab
    
> Latex: text.tex.latex

> Objective-C: source.objc

> Objective-C++: source.objc++

> YAML: source.yaml

> XML: text.xml

> SQL: source.sql

> C#: source.cs

> Java: source.java

> Javascript: source.js

> Markdown: text.html.markdown

> Python: source.python

>>>>>>> 2713152b9ea6266f9eb06355cebe34ec8f480565
> HTML: text.html(.basic)

> 可参考此处：[scopes.txt](https://gist.github.com/iambibhas/4705378#file-scopes-txt)

#### 保存新的代码片段

在保存文件对话框里，需要明确的指定文件的扩展名为.sublime-snippet，然后把文件保存到默认目录（当前用户主目录下的...\Sublime Text 3\Data\Packages\User目录中）。

#### 示例

在c++中定义一个随机数组产生子函数的代码段，如下所示：

    <snippet>
        <content><![CDATA[
    // #include <stdlib.h>
    // 产生随机数组
    template<size_t ${1:SIZE}>
    void gen_rand_n(int (&A)[${1:SIZE}])
    {
        srand(5);
        for (int i = 0; i < ${1:SIZE}; ++i)
        {
            A[i] = rand();
        }
    }
    ]]></content>
        <tabTrigger>rand</tabTrigger>
        <scope>source.c++</scope>
    </snippet>

在sublime text 3 的c++文件中，输入rand，然后按Tab键就可以自动参数此代码段。



图片懒得加了，看这里[木子超同学](http://www.muzichao.com/sublime-text-3-cuda-c-snippet/)
