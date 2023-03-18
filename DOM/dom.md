# 1.如何操作html中的元素
使用dom,文档对象模型，document object model
## 1.1获取元素1
document.getElementById返回的是html中唯一的一个元素
document.getElementsByClassName返回的是集合。也就是一个数组，如果想要某一个特定的，得像数组一样去获取到元素
document.getElementsByTagName返回的是集合
document.querySelector返回到的是指定的第一个元素，如果有多个符合，也是仅仅返回到第一个元素
document.querySelectorAll返回的是一个集合
## 1.2举例
```
<ul>
        <li id="one">1</li>
        <li class="two">2</li>
        <li class="two">3</li>
        <li class="two">4</li>
        <li>5</li>
        <li>6</li>
        <li>7</li>
    </ul>
    <button id="btn">点我修改样式</button>
    <script>
        var btn=document.getElementById('btn');
        btn.onclick=function(){
            
        var one=document.getElementById('one');
        //console.log(one);//<li id="one">1</li>
        one.style.background="red";

        var two=document.getElementsByClassName('two');
        //console.log(two);//集合//HTMLCollection(3) [li.two, li.two, li.two]
        //two.style.background="green";//报错，必须向数组一样[]去获取元素
        two[1].style.background="green";

        var lis=document.getElementsByTagName('li');
        //console.log(lis);//HTMLCollection(7) [li#one, li.two, li.two, li.two, li, li, li, one: li#one]
        lis[4].style.background="orange";

        var li=document.querySelector('.two');
        //console.log(li2);//<li class="two">2</li>//即使有多个.two,也只会获取到第一个

        var lis2=document.querySelectorAll('.two');
        //console.log(lis2);//<li class="two">2</li>//这里返回的就是一个集合了
        lis2[2].style.background="pink";

        }
    </script>
```
## 1.3获取元素2
nextElementSibling返回该节点的相邻的下一个兄弟节点
previousElementSibling返回该节点的相邻的上一个兄弟节点
parentElement返回的是该节点的父节点
children返回的是该节点的子节点的集合
## 1.4举例
```
<body>
    <ul>
        <li id="one">1</li>
        <li class="two">2</li>
        <li class="two">3</li>
        <li class="two">4</li>
        <li>5</li>
        <li>6</li>
        <li>7</li>
    </ul>
    <button id="btn">点我修改样式</button>
    <script>
        var btn=document.getElementById('btn');
        btn.onclick=function(){
        var two=document.getElementsByClassName('two');
        //two[1].nextElementSibling.background='pink';//.two第二个的下一个兄弟节点背景位粉色//也就是第4个球
        //threeball=two[1].nextElementSibling;
        //console.log(threeball);
        two[1].nextElementSibling.style.background='pink';
        two[1].previousElementSibling.style.background='#bfa';
        two[1].parentElement.style.background="skyblue";

        var uls=document.getElementsByTagName('ul');
        //console.log(uls[0].children);//返回集合
        //console.log(uls[0].children[0]);//单个元素
        uls[0].children[0].style.background='red';
        }
    </script>
</body>
```
# 2.dom操作css
## 2.1.style.属性名=""
btn.style.backgroun="#bfa";
## 2.2 .setAttribute('属性名','属性值');
btn.setAttribute('style','background:yellow;width:200px;height:200px');
## 2.3 .style.cssText='';
btn.style.cssText='background:red;width:200px'
## 2.4 classList add remove contains toggle length item
btn.classList.add('test');//添加样式，样式写在style中
btn.classList.remove('test');//删除样式
btn.classList.contains('test');//判断是否存在该样式
btn.classList.toggle('test');//切换：有则删除，无则添加
btn.classList.length;//返回class类的个数
btn.classList.item(2);//通过下标，获取class名
# 3.dom删除元素
元素.remove();
# 4.dom添加元素
添加节点 
```
            contentbox.insertAdjacentHTML(
                'beforeend',
                `<div>
                    <button class="finish">完成</button>
                    <button class="cancel">取消</button>
                    <button class="remove">删除</button>
                    <span class="spantext">${text.value}</span>
                </div>`
            );
```
