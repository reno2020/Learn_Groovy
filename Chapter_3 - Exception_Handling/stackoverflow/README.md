#### StackoverflowError 

```groovy
temp = 1

while (true)
callMe()

def callMe()
{
	println temp
	temp++
}

```

Here a method called infinite time. But it doesn't leads to the **stackoverflowError**. Here this is a another 
program,

```groovy
temp = 1

callMe()

def callMe()
{
	println temp
	temp++
	callMe()
}
```

This will leads us to **stackOverflowError**. The concept is **recursion**. 

- Instead of infinite loop, you have infinite (or very deep) recursion (function invoking itself), then you will get stack overflow. Whenever a function is invoked, some part of stack memory is consumed. Once all the stack is exhausted, you get - stack overflow error.

- Each recursive call uses some space on the stack


See the sources : [link1](https://stackoverflow.com/questions/27218736/stack-overflow-error-vs-infinite-loop), [link2](https://stackoverflow.com/questions/18368406/java-lang-stackoverflowerror-due-to-recursion)
