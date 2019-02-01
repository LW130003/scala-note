# The Scala try, catch, finally syntax (multiple exceptions, wildcard operator)
source: https://alvinalexander.com/scala/scala-try-catch-finally-syntax-examples-exceptions-wildcard

The general Scala try/catch/finally syntax looks like this:
```scala
try {
    // your scala code here
} catch {
    case foo: FooException => handleFooException(foo)
    case bar: BarException => handleBarException(bar)
    case _: Throwable -> println("Got some other kind of exception")
} finally {
    // your scala code here, such as to close a database connection
}
```

As you can see, the Scala try-catch-finally syntax is similar to the Java try-catch-finally syntax, except the *catch* area, which uses Scala's pattern  matching capabilities to handle the different exceptions you might run into.

In the example, I'm intentionally catching a FooException and a BarException, and then I am using the Scala "_" wildcard operator to catch any other exceptions that might occur.

## Using the Scala _ wildcard operator in a catch clause
One drawback of using Scala's wildcard character (_) in a catch clause is that you can't refer to it in your code, such as if you want to print the exception.

Naming your exception variable instead of using the wildcard, which you can then refer in your own code
```scala
try {
    // your scala code here
} catch {
    case foo: FooException => handleFooException(foo)
    case bar: BarException => handleBarException(bar)
    
    // handling any other exception that might come up
    case unknown => println("Got this unknown exception: " + unknown)
} finally {
    // your scala code here, such as to close a database connection
}
```
As you can see from that code, I just name a variable "unknown", which I can then refer to by name.

## Printing a Scala exception's stack trace
```scala
def runAppleScriptCommand(c: AppleScriptCommand) {
  val scriptEngineManager = new ScriptEngineManager
  val appleScriptEngine = scriptEngineManager.getEngineByName("AppleScript")
  try {
    appleScriptEngine.eval(c.command)
  } catch {
    case e: ScriptException => e.printStackTrace
  }
}
```
