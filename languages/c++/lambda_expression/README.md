
 Lambda expressions are shortcut to functions. There are many functions in the software which are called only once. So instead of creating a proper function and then calling
it once, we can use the Lambda expressions. This definition is OK but mainly they are used at places where functors (function objects, callback functions) are used. So function calls that expect callback functions can accept these lambda expressions.

Syntax is:à
[<capture list>](<arguments to lambda function>)-><return type>{<body of the function>};

capture list will have all the variables that are there in the scope in which lambda is written and have to be used inside the lambda function body.
Arguments to lambda function are like arguments passed to the function. But these will be passed by the function that calls this lambda style callback function.
return type is the type of value that will be returned by this lambda style callback functions.
body of the function has all the statements that need to be executed when this lambda style callback function is executed.

One very important benefit is that lambda expressions allow using the captured variables and arguments together. Otherwise every captured variable ned to be passed as an argument to callback function for being used inside the lambda expression.