Inside a class:à

const member variable means that its value cannot be changed once initialised. They are assigned value only inside the ctor.


constant member function is the one that makes sure that it will not make any change to any member variable. These functions cannot make use of

any non constant member variables.

constant object of a class is same as constant variable. Once created using ctor it cannot be changed.


There is no term like constant class.

Mutable keyword is used to make a non constant member variable in class to be used inside a constant member function. Even if a object of class is constant, mutable member variables can be changed.

Explicit keyword is used when the implicit conversion is not required. This implicit conversion happens only in case of single argument ctors. This is required so that accidental bugs can be avoided. For example, a function can expect an argment of type class whose ctor accepts an int. Then if the function gets called with int as an argument, imlicitly it will be converted to class object and then function will be called.


Move constructors have the purpose to transfer the ownership from the source object to the destination object. The source object will become meaningless.
The move semantics are implemented using rvalue references (&& symbols).

Example of the place where it is used is the vector storing the objects of a class. When new elements are added to the vector, the vector performs resizing so that the
elements are moved from location to other. During this, the move constructors are called.

Another place is the unique pointers. The STL implementation of this has the move constructors so that the ownership moves from one source to destination. These do not copy constructors.

Rvalue reference is the construct used when the value uses a temprary storage which will exist till the time the statement in which it is being used is getting executed and after that it has no meaning. rvalue reference binda to a temprary storage which is not usable.
Use “g++ -std=c++11 -o TestRvalue TestRvalue.cpp” as rvalue is present from c++11 onwards.