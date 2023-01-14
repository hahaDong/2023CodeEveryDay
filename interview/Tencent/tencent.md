## 腾讯面试
仓库地址：https://github.com/hahaDong/2023CodeEveryDay

### 1. 面试岗位：腾讯CSIG前端工程师

### 2. 面试进度情况
进度挺快，正常情况下2～3天会有上一轮的反馈。
+ 2022.12.6 - 邮件通知官网更新简历
+ 2022.12.9 - 一面，一小时，基础面试，无code
+ 2022.12.12 - 二面通知（约定12.14下午四点，因个人原因申请推迟至12.16下午三点）
+ 2022.12.16 - 二面，接近三小时，8道题，写完后聊了一会
+ 2022.12.27 - 三面通知（二面面试官阳了一周，因此流程卡住）
+ 2022.12.28 - 三面时长约2小时
+ 2022.12.29 - 四面通知
+ 2022.12.30 - 四面时长约1小时（个人理解为劝退面，问题领域涵盖跨端、IOS/安卓、数据库优化、深度学习）

最终告知，年底盘点HC，没信了！
 
### 3. 二面笔试题回顾

###### 笔试题1:  
```javascript
// todo
const a = [1,2,3]
a.add(2)
console.log(a) // 输出 [3,4,5]
a.add(3)
console.log(a) // 输出 [6,7,8]
```

请补充`todo`中的内容，使得以上代码执行不报错


###### 笔试题2:
请用`es5`实现一个`Event`基类，实现监听和触发自定义事件，例如包含（`on`、`emit`、`once`、`remove`等方法）另外实现一个`Page`类继承于`Event`类。

     
###### 笔试题3：
实现一个函数，输入一个整数`n`，执行后开始每隔一秒开始打印数字，从`0~n`。如：`print(10)`; 
每隔一秒`console.log` 打印 `0，1，2...10`。
尝试用尽可能多种实现方式实现该函数，其中至少需要使用一次`for`循环的实现。


###### 笔试题4：
请实现一个深克隆的方法 `deepclone`


###### 笔试题5：
以下代码的输出顺序是什么？
```javascript
console.log('script start');

setTimeout(() => {
  console.log('timeout0');
}, 0);

Promise.resolve()
.then(function() {
  console.log('promise1');
}).then(function() {
  console.log('promise2');
});


async function foo() {
  await bar()
  console.log('async1 end')
}
foo()

async function errorFunc () {
  try {
    await Promise.reject('error!!!')
  } catch(e) {
    console.log(e)
  }
  console.log('async1');
  return Promise.resolve('async1 success')
}
errorFunc().then(res => console.log(res))

function bar() {
  console.log('async2 end') 
}

console.log('script end');
```

将你认为的打印顺序依次写在此


###### 笔试题6：
要给如下所有`li`元素绑定`click`事件，在鼠标点击的时候`alert`该`li`的内容、页面中的`xy`坐标等信息。且在鼠标离开外部`ul`元素范围的时候弹出一个`alert`提示。（实现时请注意代码执行效率及浏览器兼容性、不要使用现成的框架库）


###### 笔试题7：
完成一个转换函数，将数字转成对应的大写字母，满足下面的对应关系
```
1 => A；2 => B；3 => C
...
26 => Z；

27 => AA；28 => AB；29 => AC
...
52 => AZ；

53 => BA；54 => BB
...
```


###### 笔试题8：
实现一个方法`decodeStr`，输入一个字符串，根据约定规则输出编码结果。约定规则如下：
 ```str = "2[a]1[bc]"```, 返回 ```"aabc"```.
 ```str = "2[e2[d]]"```, 返回 ```"eddedd"```.
 ```str = "3[abc]2[cd]ff"```, 返回 ```"abcabcabccdcdff"```. 
 可以看出: ```N[string]```，表示```string``` 正好重复 ```N``` 次。假设字符串一定是有效正确的字符串

