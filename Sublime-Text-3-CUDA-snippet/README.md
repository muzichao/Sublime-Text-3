### 说明

1. 在Sublime Text 3中可以通过安装`CUDA c++`插件来实现CUDA代码的高亮。安装之后位于`...\Sublime Text 3\Data\Installed Packages\`文件夹下，名字为`CUDA C++.sublime-package`。

2. 将文件的扩展名改为zip，即将`CUDA C++.sublime-package`改为`CUDA C++.zip`就可以解压。

3. 解压后的文件中包含许多以`.sublime-package`结尾的文件，这些文件就是`CUDA c++`包含的代码段（snippet）。

4. 代码段为编程提供了许多方便，但是`CUDA c++`中的代码段与Sublime Text 3自带的`C++.sublime-package`（位于`..\Sublime Text 3\Packages`文件夹下）中的代码段有许多重复的地方。会给我们的输入带来一定的困扰，鉴于此，此处对`CUDA C++.sublime-package`中的文件进行适当的修改，使其避免重复。

#### 修改

Sublime Text 3的snippet文件又一个<scope></scope>选项，
<scope>source.python</scope>的意思是说：此代码段只在python文件中起作用。

再看`CUDA C++.sublime-package`的snippet文件，其中的选项为：

    <scope>source.c, source.c++, source.objc, source.objc++, source.cuda-c++</scope>

也就是说在c，c++文件中也起作用，将其删除，修改为：

    <scope>source.cuda-c++</scope>

表示只在CUDA文件中起作用。

#### 文件说明

1. `CUDA C++.sublime-package`为修改过的`CUDA C++`插件
2. `CUDA C++.zip`为原始的`CUDA C++.sublime-package`，只是后缀名改成了zip
3. `CUDA C++`文件夹为修改过的`CUDA C++.sublime-package`文件

#### 补充

修改于Sublime Text中的`CUDA c++`文件。
地址：[CUDA C++
](https://sublime.wbond.net/packages/CUDA%20C%2B%2B)



