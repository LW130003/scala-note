# Try again, Apache Spark!
source http://rcardin.github.io/big-data/apache-spark/scala/programming/2016/09/25/try-again-apache-spark.html
Using Apache Spark throws you in a functional, distributed and asynchronous programming world. While you have not to worry about the distributed adjective, because Spark hides you every problem related to it, the *functional* and *asynchronous* adjectives make things more complex with respect to the error handling process. 

## Classical Error Handling
In classic situations, such as in languages as Java or C++, *exceptions* are used to signal an exception behavior of a program. If you need to handle a particular type of exception, you will use a **try-catch** statement, surrounding the statements that can rise the exceptions.

```scala
try {
    // This method can rise an Exception
    someMethod()
} catch (Exception e) {
    // Handle the exception behavior in some way
}
```

In Scala language the above statements become as follow
```scala

```
