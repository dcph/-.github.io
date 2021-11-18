1.replace()

对象.replace(rgExp,replaceText,max)

其中，rgExp和replaceText是必须要有的，max是可选的参数，可以不加。
rgExp是指 String 对象或文字；replaceText是一个String 对象或字符串文字；max是一个数字。对于一个对象，在对象的每个rgExp都替换成replaceText，从左到右最多max次。

2.python中的正则化表达式

3.python选取某一时间段数据

（1）datetime( )，获取指定的时间和日期。datetime(%Y,%m,%d,%H,%M,%S)

datetime共有6个参数，分别代表的是年月日时分秒。其中年月日是必须要传入的参数，时分秒可以不传入，默认全为零。

datatime.strptime将Str转化为datetime

意到datetime是模块，datetime模块还包含一个datetime类，通过from datetime import datetime导入的才是datetime这个类。如果仅导入import datetime，则必须引用全名datetime.datetime

（2）pd.to_datetime( )，pandas中的to_datetime( )有和datetime( )类似的功能。

pd.to_datetime( '2017/09/24 11:38:30',format='%Y /%m/%d %H:%M:%S ')，获取指定的时间和日期。

pd.to_datetime( data,format='%Y /%m/%d %H:%M:%S ')，转化为时间格式

4.map() 

会根据提供的函数对指定序列做映射。第一个参数 function 以参数序列中的每一个元素调用 function 函数，返回包含每次 function 函数返回值的新列表。

map(function, iterable, ...)

function -- 函数，iterable -- 一个或多个序列

返回一个迭代器

5.DataFrame选取

df['A'],选取列，df['A','B'],选取多列，df.loc[[1,3]],选取多行，df.loc[1:3],选区连续多行，df.loc[1:3,'A'],选取范围多行，df.iloc[1:3,1:3]，选区连续多行与连续多列

6.pd.DateOffset()

pd.DateOffset()：时间戳的加减

DateOffset常用的参数：
months，设置月。
days，设置天。
years，设置年。
hours，设置小时。
minutes，设置分钟。
seconds，设置秒。

pd.to_datetime('2020-03-14')+pd.DateOffset(days=10)

输出：Timestamp('2020-03-24 00:00:00')

DateOffset参数也可以组合使用：pd.to_datetime('2020-03-14')+pd.DateOffset(months=1,days=10,hours=2)

输出：Timestamp('2020-04-24 02:00:00')

7.LabelEncoder

LabelEncoder是用来对分类型特征值进行编码，即对不连续的数值或文本进行编码。其中包含以下常用方法：

fit(y) ：fit可看做一本空字典，y可看作要塞到字典中的词。

fit_transform(y)：相当于先进行fit再进行transform，即把y塞到字典中去以后再进行transform得到索引值。

inverse_transform(y)：根据索引值y获得原始数据。

transform(y) ：将y转变成索引值。

8.rename

用于列名重命名

colNameDict = {'源数据列名':'新列名'}                  #将‘源数据列名’改为‘新列名’

df.rename(columns = colNameDict,inplace=True)

9.intersection()，difference（）

set.intersection(set1, set2...etc)

set1 - - 必需，要查找相同元素的集合。set2 - - 可选，其他要查找相同元素的集合，可以多个，多个使用逗号, 隔开。返回一个新集合，计算两个集合的交集


set.difference(set1, set2...etc)

set1 - - 必需，要查找相同元素的集合。set2 - - 可选，其他要查找相同元素的集合，可以多个，多个使用逗号, 隔开。返回一个新集合，计算两个集合的并集

10.enumerate() 

用于将一个可遍历的数据对象(如列表、元组或字符串)组合为一个索引序列，同时列出数据和数据下标，一般用在 for 循环当中。

enumerate(sequence, [start=0])

sequence -- 一个序列、迭代器或其他支持迭代对象

start -- 下标起始位置。

返回 enumerate(枚举) 对象。

11.toList()

把****转化为List集合

12.reset_index()

df = df.reset_index(drop=True)

reset_index经常使用的地方是处理groupby（）方法调用后的数据,将原来的index设置为列,如果index没有名称，那么默认列名为index。可以通过df.index.name指定了列名之后再调用该方法

13.
