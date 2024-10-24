# 引用与创建DataFrame

在创建DF表格时，我们得先引入Pandas模块，就像其他模块一样引入：

```python
import pandas as pd
```

这样，我们就可以把Pandas模块给引入了。同时，我们把pandas指令给缩写成了`pd`。在以后的学习中，我们将会用pd来指代Pandas。

我们可以用Python里面自带的数组或列表来创建一个DataFrame表格。在考场中，一般不会考查你是否会创建表格。以下是一个例子：

```python

import pandas as pd

# 假设你有一个嵌套的数组（列表）
data = [
    [1, 'Alice', 25],
    [2, 'Bob', 30],
    [3, 'Charlie', 35]
]

# 创建一个DataFrame，指定列名
df = pd.DataFrame(data, columns=['ID', 'Name', 'Age'])

# 打印表格
print(df)

```


假设你有一个嵌套的数组，数组里面每一个元素都有几个数值。在以上的例子中，我们将每个元素都写入了ID、姓名以及年龄三个数据，并举例了3个元素。

此时，我们使用`pd.DataFrame()`指令来创建一个DataFrame表格。我们会在括号内加入一些必要的描述，以便电脑知道我们要做成什么样的DF表格。

`df = pd.DataFrame(data, columns=['ID', 'Name', 'Age'])`

在`pd.DataFrame()`中，我们填入了两个描述：1.表格内数据；2.表格的Column标签数据（每列的名称）。如：

```python
pd.DataFrame(【表格数据】,【Column数据】)

# 在这个指令中，我们除了必须填入表格数据之外，我们还可以填入其他的描述。例如，我们可以规定表格只显示某些数据或者让表格按从小到大的顺序排序。我们会在以后的课程中学到相关内容。

```

我们现在再回到刚才的代码上
`df = pd.DataFrame(data, columns=['ID', 'Name', 'Age']) `
你是否发现了我们在代码的开头有一个“df = ”呢？为什么我们要把创建好的DF表格赋予给一个叫df的变量呢？

是因为 **DF表格创建完成后是不会被保存的，而我们需要手动将表格保存到一个特定的变量上。** 在以后对表格每次进行修改，我们都要像这样子“保存”一下，将修改后的内容保存到一个变量中。

最后，我们输入了`print(df)`代码来让表格显示在屏幕上。看看我们刚才创建的表格吧：
```python
输出结果：

   ID     Name  Age
0   1    Alice   25
1   2      Bob   30
2   3  Charlie   35

```


