闭包

1.启示：
    a.js中闭包无处不在，你只需要能够识别并拥抱它。
    b. 闭包是基于词法作用域书写代码时所产生的自然结果。

2.实质问题
    a. 当函数可以记住并访问所在的词法作用域时，就产生了闭包，即使函数是在当前词法作用域之外执行。

    function foo () {
        var a = 2;

        function bar（） {
            console.log(a)
        }
        return bar;
    }

    var baz = foo();
    baz();

    b. 无论通过何种手段将内部函数传递到所在的词法作用域以外，它都会持有对原始作用域的引用，无论在何处执行这个函数都会使用闭包。

3. 现在我懂了
    在定时器、事件监听器、Ajax请求、跨窗口通信、web worker 或者任何其他异步（同步）任务中，只要使用了回调函数，实际上就是在使用闭包

4. 循环和闭包