2019复习-Android

# Android四种启动模式

> standard:默认模式

	在启动此Activity的Activity栈中创建一个新的实例


> singleTop:栈顶复用

	当所被调用的Activity已经位于栈顶，则直接调用onNewIntent方法(可由此取出当前请求的信息)，不会创建新实例，也不调用onCreate,OnStart；否则创建新实例

> singleTask:栈内复用

	一种单例模式，并在调用时可以指定任务栈
	当已经存在此实例时，回调onNewIntent方法
	具有clearTop属性（弹出对应实例之上的所有实例）

> singleInstance:单实例模式
	
	加强的singleTask模式，具有所有的singleTask属性
	具有单独的任务栈，除非整个任务栈被销毁，否则不会创建新实例
	
