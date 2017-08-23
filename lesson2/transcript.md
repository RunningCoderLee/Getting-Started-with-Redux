`The second principle of Redux is that the state tree is read only. You cannot modify or write to it. Instead, anytime you want to change the state, you need to dispatch an action.`

`Redux`的第二个原则是state树是只读的。你不能修改或者写入它。取而代之的是，任何时候你想要修改state时，你都需要dispatch一个action

`An action is a plain JavaScript object describing the change. Just like the state is the minimal representation of the data in your app, the action is the minimal representation of the change to that data.`

一个action是一个描述变化的简单JavaScript对象，就像state是你应用中数据的最小表示一样，action是对数据更改的最小表示

`The structure of the action object is up to you. The only requirement is that it has a tie property, which is not undefined. We suggest using strings, because they are serializable.`

action对象的结构由你来决定，唯一的要求是它有一个没有定义的绑定属性。我们建议使用字符串，因为它们是可序列化的

`In different apps, you're going to have different types of actions. For example, in a counter app we only have increment and decrement actions. We don't pass any additional information, because this is all that is needed to describe these changes.`

在不同的app中，你可能会有不同类型的actions。举个例子，在一个计数应用中，我们只需要增加和减少的actions。因为所有需要用来描述改变的信息都在这里了，所以我们不传递任何额外的信息。

`But say, for a counter release example, we have more actions. We have add counter action, we have a remove counter action, and anytime I change the individual counter, you can see that the increment and the decrement actions now have index. Because we need to describe which particular counter was changed.`

但是，对于一个计数器发布示例，因为我们需要描述特定的计数器发生了变化，因此我们需要有更多的actions。添加计数action，删除计数action，每当我改变一个计数器，你就可以看到增加和减少的actions现在有了索引。


`This approach scales well to medium and complex applications. Anytime I add a todo, the components don't really know how exactly it's been added. All they know is that they need to dispatch an action with a type, add todo, and the text of the todo and a sequential ID.`

这可以很好的适应中等或复杂的应用。任何时候我添加一个待办事项，组件不需要真正了解它是如何被添加进来的。它们所要了解的仅仅是需要dispatch一个带有待办事项类型和待办事项内容以及表明顺序的id的action

`If I toggle a todo, again, the components don't know how it happens. All they need to do is to dispatch an action with a type, toggle todo and pass in the ID of the todo I want to toggle.`

如果我再次切换一个待办事项，组件不知道它是如何发生的，他只需要dispatch一个带有我想要切换的待办事项id，并且标明切换待办事项为已完成类型的action即可。

`The same is true for the visibility filter. Anytime I click on this control to change the currently visible todos, what really happens is this component dispatches an action with a type, set visibility filter, and pass in the desired filter string, filter filled.`

对过滤器的选择也一样，任何时候我点击控件用来更改当前显示待办事项状态的时候，真正发生的只是组件dispatch一个标明设置可见性过滤器类型并且传入所需的过滤器字符串，过滤器填充。


`But these are all plain objects, describing what happens in a wrap.`

但是这些都是被包装起来的简单对象，用来描述发生了什么

`Now you know the second principle of Redux -- the state is read only. The only way to change the state tree is by dispatching an action. An action is a plain JavaScript object, describing in the minimal way what changed in the application. Whether it is initiated by a network request or by user interaction, any data that gets into the Redux application gets there by actions.`

现在你了解了`Redux`的第二个原则 -- state是只读的。改变state树的唯一途径是dispatch一个action。一个action是一个简单的JavaScript对象，用最小的方式来描述在应用中发生了什么改变。无论是通过网络请求还是用户交互来初始化，进入Redux应用程序的任何数据都会通过actions获取