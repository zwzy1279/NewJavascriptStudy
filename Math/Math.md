# Math
Math对象不用new，直接打点访问里面的属性或者方法
# Math对象的属性
Math.PI 返回数字
Math.E          // 返回欧拉指数（Euler's number）
Math.PI         // 返回圆周率（PI）
Math.SQRT2      // 返回 2 的平方根
Math.SQRT1_2    // 返回 1/2 的平方根
Math.LN2        // 返回 2 的自然对数
Math.LN10       // 返回 10 的自然对数
Math.LOG2E      // 返回以 2 为底的 e 的对数（约等于 1.414）
Math.LOG10E     // 返回以 10 为底的 e 的对数（约等于 0.434）
# Math对象的方法
## 关于取舍
Math.ceil()向上取舍，不论是1.4还是1.5，结局都是2
Math.floor()向下取舍，不论是1.5还是1.4，结局就是1
Math.round()四舍五入，1.4结果是1，1.5结果是2
## 关于生成数字
### 随机数
Math.random()介于0-1之间的小数（0，1）开区间，都不会取到
### 生成1-10之间的数字，闭区间
Math.random()*10
## 关于比较
Math.max()//返回最大值
Math.min()//返回最小值
## 关于绝对值
Math.abs()//返回绝对值
## 关于计算
Math.pow(x,y);//返回x的y次幂
Math.sqrt(x);//返回x的平方根

