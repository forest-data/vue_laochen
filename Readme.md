# 1.什么是双向绑定？    MVVM
# M数据改变，V页面数据也变。

# 2. Vue-cli 脚手架 打包工具
# 用来编译用的

# 3. 
<h3 v-if="isVip">用户类型: VIP</h3>   直接没有该元素
<h3 v-show="isVip">用户类型: VIP</h3>    就是设置display

# 4.   :绑定     @事件

# 5. 为什么li循环哪里需要加 key ? 
# 因为要告知vue,每一个对象都是独一无二的。如果不告诉vue就懒加载，就是针对值的改变
# key就是用来做一个标识的

# 6.
<li v-for="item,index in students" v-if="item.age%2!=0" :key="index"></li>

# 7. 什么叫xss攻击？
htmlTxt: '<span>hello</span><script src="js/hello.js"></script>'

# 8. 如果要在 {{}} 写复杂的表达式，用计算属性和侦听器
{{isVip? '欢迎光临': '走开'}}  简单的表达式

建议条件渲染和列表渲染不要一起使用，因为每次循环都要去判断，影响性能
推荐使用计算属性

# 箭头函数 (item, i)=>{}   等价于   匿名函数  function(item, i){}   见 05计算属性

# 9. 侦听器 > 监听数据变化的事件 监听数据改变的时候触发事件，监听data数据

# 10. computed计算属性 > console.log(this) //this指向app