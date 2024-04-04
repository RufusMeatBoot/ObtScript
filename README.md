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
> newObject {
>    nestedObject1 {
>        Int: x = 1
>        String: h = "hello world"
>        Bool: y = true
>        Float: i = 2.9
>        Arr: j = [1, 2, 3, 4]
>    }
>    nestedObject2 {
>        Int: x = newObject.nestedObject1.x
>        String: h = newObject.nestedObject1.h
>        Bool: y = newObject.nestedObject1.y
>        Float: i = newObject.nestedObject1.i
>        Arr: j = newObject.nestedObject1.j
>    }
> }
> ```
