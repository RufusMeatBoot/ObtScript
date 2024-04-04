# ObtScript
> **A general purpose object based language for storing complex datasets.**

# Features
> **ObtScript inlcudes many features, such as value inheritance, nested objects, and express datatypes**
> - ObtScript is intended to be used as an alternative to JSON, allowing for more precise data management and options for storing values

# Examples
> **Creating an Object**
> - Objects are as simple as defining an object name, followed by the contents of your object, such as `yourObject {}`

> **Declaring Values Inside Objects**
> - Values can be added to objects by first declaring their type, followed by their values, such as `Int: x = 4`

> **Supported Datatypes**
> - Integers
> - Floating Points
> - Booleans
> - Strings
> - Arrays

> **More Information**
> - Objects can be nested within other objects, known as `parent` and `child` objects.
> - Objects can inherit values from other objects

# Putting it All Together
> ```
> _OBJECT {
>     _NESTED {
>         i_INT   : 1
>         s_STR   : "hello world"
>         b_BOOL  : true
>         f_FLOAT : 2.9
>         a_ARR   : [1, 2, 3, 4]
>     }
>     _NESTED {
>         i_INT   : $_OBJECT._NESTED.i_INT
>         s_STR   : $_OBJECT._NESTED.s_STR
>         b_BOOL  : $_OBJECT._NESTED.b_BOOL
>         f_FLOAT : $_OBJECT._NESTED.b_FLOAT
>         a_ARR   : $_OBJECT._NESTED.a_ARR
>     }
> }
> ```
