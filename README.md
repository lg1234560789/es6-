# es6-


1. map
map函数可以看成是一种映射函数，而且是一一映射

array.map(function(参数){

....

函数体

......

})

es6写法：
array.map((参数)=>{

....

函数体

......

})



map适合对一个数组中的每个元素进行相同的操作



2. filter
filter函数可以看成是一个过滤函数，返回符合条件的元素的数组

filter和map的区别：filter需要在循环的时候判断一下是true还是false，是true才会返回这个元素；map没有这个过程。

array.filter((参数) => {

	函数体

})



filter函数适合筛选一个数组中满足条件的元素，注意：filter函数只是筛选功能，不能改变元素、操作元素

3. reduce
reduce函数可以理解成一个迭代函数

例子1：

sameLayerExps.reduce((sum: number, exp: Experiment) => sum += exp.traffic, 0)


例子2：返回所有试验名称组成的数组

    experiments.reduce( (names: Array<string>, o) => {
        names.push(o.name);
        return names;
    }, []);

例子3：



array.reduce((previous, current, index, array) =>{

	函数体

}, [initialValue])

reduce函数有四个参数：之前值，当前值，索引值，数组本身。

previous值取决于[initialValue]

如果指定[initialValue]指定是，则作为previous的初始值，也可作为空数组[]，

如果缺省的话，则将数组的第一个元素作为previous的初始值，下次循环时，之前值就是上一次的当前值，而当前值会变成下一个索引对应的元素，依次类推。

4. find
查找到第一个符合条件的元素，则立刻返回

