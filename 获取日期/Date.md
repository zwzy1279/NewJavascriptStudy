# Dath对象
## Dath对象是什么
Date对象用于处理日期和时间，Date对象在使用时需要new创建实例，通过实例来对对象中的属性和方法进行处理。通过打点访问对象中的属性和方法。
## Date对象属性
constructor
prototype
## Date对象方法
获取指定时间的年月日
获取从1970年1月1日到现在的毫秒数
## 倒计时案例
指定截止日期（new Date中可以放入时间）如：let date=new Date('2022-04-05 9:00:01')
获取从1970年1月1日到现在的毫秒数，通过/1000转成秒，通过/60转成分钟，通过/60转成小时，通过/24转成每天，通过/365转成每年

