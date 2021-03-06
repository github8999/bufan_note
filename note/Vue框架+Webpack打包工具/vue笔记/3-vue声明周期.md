##  什么是生命周期
+   **声明周期:** 
    
    **生命周期,** 指从vue实例创建,运行,到销毁期间;伴随着各式各样的事件,这些事件统称为生命周期;
---
+   **生命周期钩子**
    
    **生命周期钩子,** 指的是生命周期函数的别名; 生命周期钩子 == 生命周期函数 == 生命周期事件

+   **生命周期函数分类**
    
    1. **创建期间** 的生命周期钩子
        
        a) beforeCreate :表示刚初始化了一个空的实例,身上只有一些默认的事件和生命周期函数, 其他的属性和方法都未创建; ( 在beforeCreate生命周期 函数执行的时候, data 和 methods 中的 数据 都还没有初始化 )

        b) created :这个时候data和methods中的数据已经初始化完毕, 如果要使用data和methods中的数据最早只能在create中操作;

        c) beforeMount :这里表示已经把 #app模板 编译完成了 但是尚未渲染到页面中; 此时输出dom节点中的数据仍为 mustache插值;

        d) mounted :这里表示已经把内存中编译好的模板,挂载到页面中去,用户已经可以看到渲染好的页面了; 这时 mustache插值 已经被替换为 前端model层中 data 和 methods 中的数据, 此时如果没有别的操作,该实例就静静的在内存中发呆;

    2. **运行期间** 的生命周期钩子 

        - 运行期间的两个事件, 当data改变的时候会被调用, 有选择的时候触发 0 到 n 次

        a) beforeUpdate: 该事件执行的时候, data中的数据已经改变, 但是尚未渲染到页面中的dom元素中; 这个时候打印data中的数据,和从dom中获取该数据是不一致的;

        b) update: 该事件执行的时候, data中的数据已经改变且已经同步到页面中去了; 这时打印data中的数据 和 从dom中获取的数据是一致的;

    3. **销毁期间** 的生命周期钩子

        a) beforeDestroy: 当调用vm.$destroy() 的时候,该实例开始被销毁, 此时开始调用beforeDestroy ,但是 vue实例 身上基本所有的属性都仍然可用;

        b) destroyed: 当对象中所有的内容都已经销毁后调用destroyed 结束 vue实例的生命;







