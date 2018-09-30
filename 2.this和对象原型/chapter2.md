this 全面解析

    1.调用位置：
        调用位置就是函数在代码中被调用的位置。
        最重要的是要分析调用栈

    2. 绑定规则

        1.默认绑定：

        function foo() {console.log(this.a)} // 此时很熟调用时应用了this的默认绑定，因此this指向全局对象

        2.隐式绑定：

        function foo() {console.log(this.a)};
        var obj = {
            a: 2,
            foo: foo
        }
        obj.foo();