## 1.javascript字符串分类
可以是原始值，通过字面方式创建
```
var name="Amy";//typeof name返回string
```
也可以通过关键词new定义对象
```
var name=new String('Amy');//typeof name 返回object
```

不论是哪种方式创建的字符串，都可以访问到字符串对象中的属性或者方法
## 2.字符串属性
length
```
var name="Amy";
console.log(name.length);
```
## 3.字符串方法
### 3.1查找
indexOf()返回字符串中指定文本首次出现的索引（下标）
lastIndexOf()返回指定文本在字符串中最后一次出现的索引
//如果没有找到相对应的索引，则返回-1

search()返回字符串中指定文本首次出现的索引（下标）
### 3.2提取部分字符串
slice(start, end)//返回被提取的部分
substring(start, end)
substr(start, length)
//substring() 类似于 slice()。
不同之处在于 substring() 无法接受负的索引。
substr() 类似于 slice()。
不同之处在于第二个参数规定被提取部分的长度。
### 3.3替换字符串内容
replace(x,y);//用y替换x//返回替换的结果
### 3.4转成大小写
toUpperCase() 把字符串转换为大写，返回转成大写的结果
toLowerCase() 把字符串转换为小写
### 3.5连接
concat() 连接两个或多个字符串，返回连接后的结果
### 3.6String.trim()
trim() 方法删除字符串两端的空白符：//返回删除完空格的结果
### 3.7提取字符串字符
charAt() 方法返回字符串中指定下标（位置）的字符串
charCodeAt() 方法返回字符串中指定索引的字符 unicode 编码
### 3.8把字符串转换为数组
split() 将字符串转换为数组：返回用指定分隔符分隔的单个字符的数组
## 4.模板字面量
模板字面量使用反引号 (``)来定义字符串
可以在字符串中同时使用单引号和双引号
字符串插值${...}可以将变量和表达式插入字符串
```
let price = 10;
let total = `Total: ${price}`;//Total；10
```