# ObtScript
> **A general purpose object based language for storing complex datasets.**

# Features
> **ObtScript inlcudes many features, such as value inheritance, nested objects, and express datatypes**
> ObtScript is intended to be used as an alternative to JSON, allowing for more precise data management and options for storing values

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
> - Characters
> - Enumerated Lists
> - Arrays

> **More Information**
> - Objects can be nested within other objects, known as `parent` and `child` objects.
> - Objects can inherit values from other objects

# Putting it All Together
> ```
> newObject {
>    nestedObject1 {
>        Int: x = 1
>        String: h = "hello world"
>        Bool: y = true
>        Float: i = 2.9
>        Char: o = "p"
>        Arr: j = [1, 2, 3, 4]
>        Enum: g = [
>            one = 1
>            two = 2
>        ]
>    }
>    nestedObject2 {
>        Int: x = new_object.x
>        String: h = new_object.h
>        Bool: y = new_object.y
>        Float: i = new_object.i
>        Char: 0 = new_object.object.o
>        Arr: j = new_object.j
>        Enum: g = new_object.g
>    }
> }
> ```
