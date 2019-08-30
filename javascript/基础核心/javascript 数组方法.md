#### 操作数组的基本方法

```javascript
// 1.连接两个或更多的数组，并返回结果。
Array.concat()
// 2.把数组的所有元素放入一个字符串。元素通过指定的分隔符进行分隔。
Array.join()
// 3.删除并返回数组的最后一个元素
Array.pop()
// 4.向数组的末尾添加一个或更多元素，并返回新的长度。
Array.push()
// 5.颠倒数组中元素的顺序。
Array.reserve()
// 6.删除并返回数组的第一个元素
Array.shift()
// 7.从某个已有的数组返回选定的元素
Array.slice()
// 8.对数组的元素进行排序
Array.sort()
// 9.删除元素，并向数组添加新元素。
Array.splice()
// 10.返回该对象的源代码。
Array.toSource()
// 11.把数组转换为字符串，并返回结果。
Array.toString()
// 12.把数组转换为本地数组，并返回结果。
Array.toLocalString()
// 13.向数组的开头添加一个或更多元素，并返回新的长度。
Array.unshift()
// 14.返回数组对象的原始值
Array.valueOf()
// 15.排序
Array.sort()
// 16.查找
Array.indexOf()/Array.lastIndexOf()
```

#### ES5数组迭代方法

### `IE9+、Firefox 2+、Safari 3+、Opera 9.5+和 Chrome)`

```javascript
// 用于替代for循环，比for循环简便，但不能随意退出，不能使用break。此方法没有返回值。
Array.forEach()
// 返回的是一个数量相等的新数组，返回的内容是什么取决于在fn中返回的值。
map(fn)
适用于数组中的对象，不会改变原数组。
// 返回一个新数组，包含通过callback函数测试的所有元素。
filter(fn)  
利用这个方法对数组元素进行筛选。
// 合并多个数组，返回合并后的新数组，原数组没有变化
concat()
// 如果该函数对任何一项返回ture,则返回ture。
some(fn);
// 执行函数时，所以都返回ture,则返回ture。
every(fn):
```

#### 数组归并方法 reduce

```javascript
reduce()和 reduceRight()，这两个方法都会迭代数组的所有项，然后构建一个最终返回的值。
其中，reduce()方法从数组的第一项开始，逐个遍历到最后。而 reduceRight()则相反。
这两个方法都接收两个参数：一个在每一项上调用的函数和（可选的）作为归并基础的初始值。
给 reduce()和 reduceRight()的函数接收 4 个参数：前一个值、当前值、项的索引和数组对象。这个函数返回的任何值都会作为第一个参数自动传给下一项。
第一次迭代发生在数组的第二项上，因此第一个参数是数组的第一项，第二个参数就是数组的第二项；
① reduce() 只有一个参数：函数
② reduce()  两个参数：函数，归并初始值；
③ reduceRight()和reduce()的作用一样，但是遍历方向相反
④ 应用例题，（参考 https://www.jianshu.com/p/2d396b10afe0）
var str = 'name, age, hair\nMerble, 35, red\nBob, 64, blonde';
处理str，得到 [["name", "age", "hair"], ["Merble", "35", "red"],["Bob", "64", "blonde"]];
```

#### ES6 数组方法

```
Array.from()
Array.of()
entries()，keys() 和 values()
```



#### ES7数组方法

```javascript
Array.prototype.includes
```

