# ObtScript
> **A general purpose object based language for storing complex datasets.**

# Features
> **ObtScript inlcudes many features, such as value inheritance, nested objects, and express datatypes**
> - ObtScript is intended to be used as an alternative to JSON, allowing for more precise data management and options for storing values

# Examples
> **Creating an Object**
> - Objects are as simple as defining an object name, followed by the contents of your object, such as `yourObject {}`

> **Declaring Values Inside Objects**
> - Values can be added to objects by first declaring their name, followed by their values, such as `x : 4`

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
> ` Define the base configuration for a generic vehicle `
> _VEHICLE_CONFIG {
>     _BASE {
>         brand: "Generic Motors"
>         color: "Black"
>         max_speed: 150
>         fuel_capacity: 50
>     }
> }
> 
> ` Define a configuration for a car inheriting from the generic vehicle configuration `
> _CAR_CONFIG {
>     _BASE {
>         ` Inherit base properties from VEHICLE_CONFIG `
>         brand: $_CAR_CONFIG._BASE.brand
>         color: $_CAR_CONFIG._BASE.color
>         max_speed: $_CAR_CONFIG._BASE.max_speed
>         fuel_capacity: $_CAR_CONFIG._BASE.fuel_capacity
> 
>         ` Car-specific properties `
>         num_doors: 4
>         has_sunroof: true
>     }
> }
> 
> ` Define a configuration for a motorcycle inheriting from the generic vehicle configuration `
> _MOTORCYCLE_CONFIG {
>     _BASE {
>         ` Inherit base properties from VEHICLE_CONFIG `
>         brand: $_MOTORCYCLE_CONFIG._BASE.brand
>         color: $_MOTORCYCLE_CONFIG._BASE.color
>         max_speed: $_MOTORCYCLE_CONFIG._BASE.max_speed
>         fuel_capacity: $_MOTORCYCLE_CONFIG._BASE.fuel_capacity
> 
>         ` Motorcycle-specific properties `
>         has_sidecar: false
>         is_sportbike: true
>     }
> }
> ```
