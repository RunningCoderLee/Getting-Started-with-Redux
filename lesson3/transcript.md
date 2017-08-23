`Before we proceed any further, it's important that you understand the difference between the pure and impure functions. The pure functions are the functions whose returned value depends solely on the values of their arguments.`

在我们继续进行之前，理解纯函数和非纯函数之间的区别很重要。纯函数即返回值仅取决于函数参数

`Pure functions do not have any observable side effects, such as network or database calls. The pure functions just calculate the new value. You can be confident that if you call the pure function with the same set of arguments, you're going to get the same returned value. They are predictable.`

纯函数没有任何可预测到的副作用，比如网络请求或数据库调用。纯函数只是计算新值。你可以确信，如果你调用传入相同参数的纯函数时，那么你总会获得相同的返回值。它们是可以被预见的。

`Also, pure functions do not modify the values passed to them. For example, squareAll function that accepts an array does not overwrite the items inside this array. Instead, it returns a new array by using items map.`

此外，纯函数不会修改传入的参数，比如，接收数组参数的squareAll函数不会覆盖此数组内的元素，而是通过遍历元素返回一个新数组

`On the opposite, impure functions may call the database or the network, they may have side effects, they may operate on the DOM, and they may override the values that you pass to them. This is going to be an important distinction because some of the functions that you're going to write in Redux have to be pure, and you need to be mindful of that.`

相反，非纯函数可能会调用数据库或发起网络请求，它们可能引起副作用，它们可能在DOM上操作，可能会改写你传入的值。你在`Redux`中编写的一些函数必须是纯函数，你需要注意，这将是一个非常重要的区别。
