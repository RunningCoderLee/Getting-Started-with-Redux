`The first principle of Redux is whether your app is a really simple one like this counter example, or a complex application with a lot of UI, and change of state, you are going to represent the whole state of your application as a single JavaScript object.`

Redux的第一个原则是，无论您的应用程序是一个像计数器示例这样的非常简单的应用，还是具有大量UI和状态更改的复杂应用，您都需要将应用程序的整个状态表示为单个JavaScript对象。

`All mutations, and changes the state in Redux are explicit. It is possible to keep track of all of them. In this case, I am logging every state change in the application in the console. You can see that, in the counter example, there isn't really much state to keep track of so it can be represented by a JavaScript number.`

所有的突变以及在Redux中状态的改变都是明确的。我们可以追踪所有这边变化。在这种情况下，我可以在控制台中记录应用程序中每一次状态的改变。你可以看到，在计数器实例中，没有太多状态来进行追踪，因此可以通过一个JavaScript数字来表示


`Here is a different example, a list of independent counters that I can add and remove. In this case, a single number is not enough to represent the state of the application, so we use an array of JavaScript numbers. In a more complex application, there is more state to keep track of.`

这是一个不同的例子，我可以添加和删除一个独立计数器的列表。在这种情况下，单个数字不足以表示应用程序的状态，因此我们使用一个包含JavaScript数字的数组。在更复杂的应用中，有更多的状态来跟踪。

`This is a typical to-do app, where I can add to-dos, I can cross them as completed ones, and I can change their current filter. Looking back at the history of the state changes, we can see that the initial state of the app was a JavaScript object, containing an array under the to-do string, and a string seen show all, under visible, the filter.`

“这是一个典型的to-do应用程序，我可以在其中添加任务，我可以将它们变成已完成的任务，我可以更改其当前的过滤器。 回顾状态更改的历史记录，我们可以看到应用程序的初始状态是一个JavaScript对象，其中包含一个在to-do字符串下的数组，另一个show_all字符串显示在visiblilityFilter字符串下。

`When I added the first to-do, it was added to the to-dos array, inside our state object. The to-do itself, is described by a plain child script object, saying it was not completed, and the text was saved. Every further change that the app, whether when I was crossing out the to-dos, or when I changed the visibility filter, resulted in this change to this state object, described in our whole application.`

当我添加第一个待办事项时，它被添加到我们的状态对象内的to-dos数组。 待办事项本身由简单的子脚本对象描述，表示尚未完成，文本已被保存。 应用程序的每一个进一步的变化，无论是当我正在完成待办事项，或者当我改变可见性过滤器时，都会导致这种状态对象的改变，这在我们整个应用程序中都有描述。

`Now you know the first principle of Redux, which is that, everything that changes in your application, including the data and the UI state, is contained in a single object, we call the state or the state tree.`

现在你知道Redux的第一个原理是应用程序中所有改变的内容（包括数据和UI状态）都包含在一个对象中，我们称之为state或state tree