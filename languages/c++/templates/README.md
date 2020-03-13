Templates are classes that are having generic data type. The code is replicated for every data type that is used to call the template. This happens at compile time.
If the template has static variable, then every copy of class created from template for each data type will be have its own static variable.

It is also possible to provide a specific implementation of the template for some specific data types. This is called template specialization.