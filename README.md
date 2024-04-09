
# ObtScript Documentation

### Introduction

ObtScript is a versatile, intuitive alterative to JSON. 

#

### Syntax Overview

ObtScript offers a simple and intuitive syntax, consisting of key components:

* Objects: Represent structured data containers.
* Properties: Define attributes within objects.
* Inheritance: Allows objects to inherit properties from other objects.
* Comments: Provide explanatory notes within the code.

#
  
# Structure

### Objects

Objects encapsulate related properties within a named container.

```
OBJECT_NAME {
    PROPERTY_1: VALUE_1
    PROPERTY_2: VALUE_2
    ...
}
```

#

### Properties

Properties consist of key-value pairs defining attributes within objects.

```
PROPERTY_NAME: VALUE
```

#

### Inheritance

Inheritance enables objects to inherit properties from other objects.

```
OBJECT_NAME {
    PROPERTY_1: $PARENT_OBJECT.PROPERTY_1
    PROPERTY_2: $PARENT_OBJECT.PROPERTY_2
    ...
}
```

#

### Comments

Comments provide additional context and explanatory notes within the code.

```
` This is a comment `
```

#

# Usage

### Creating Objects

To define a new object, specify its name followed by a block of properties enclosed in curly braces.

```
OBJECT_NAME {
    PROPERTY_1: VALUE_1
    PROPERTY_2: VALUE_2
    ...
}
```

#

### Putting it Together

```
` Define the base configuration for a generic vehicle `
VEHICLE_CONFIG {
    BASE {
        brand: "Generic Motors"
        color: "Black"
        max_speed: 150
        fuel_capacity: 50
    }
}

` Define a configuration for a car inheriting from the generic vehicle configuration `
CAR_CONFIG {
    BASE {
        ` Inherit base properties from VEHICLE_CONFIG `
        brand: $VEHICLE_CONFIG._BASE.brand
        color: $VEHICLE_CONFIG._BASE.color
        max_speed: $VEHICLE_CONFIG._BASE.max_speed
        fuel_capacity: $VEHICLE_CONFIG._BASE.fuel_capacity

        ` Car-specific properties `
        num_doors: 4
        has_sunroof: true
    }
}

` Define a configuration for a motorcycle inheriting from the generic vehicle configuration `
MOTORCYCLE_CONFIG {
    BASE {
        ` Inherit base properties from VEHICLE_CONFIG `
        brand: $VEHICLE_CONFIG._BASE.brand
        color: $VEHICLE_CONFIG._BASE.color
        max_speed: $VEHICLE_CONFIG._BASE.max_speed
        fuel_capacity: $VEHICLE_CONFIG._BASE.fuel_capacity

        ` Motorcycle-specific properties `
        has_sidecar: false
        is_sportbike: true
    }
}

` Sample output chart generation
VEHICLE_CONFIG
└── BASE
    ├── brand ➝ "Generic Motors"
    ├── color ➝ "Black"
    ├── max_speed ➝ 150
    └── fuel_capacity ➝ 50
CAR_CONFIG
└── BASE
    ├── brand ➝ "Generic Motors"
    ├── color ➝ "Black"
    ├── max_speed ➝ 150
    ├── fuel_capacity ➝ 50
    ├── num_doors ➝ 4
    └── has_sunroof ➝ true
MOTORCYCLE_CONFIG
└── BASE
    ├── brand ➝ "Generic Motors"
    ├── color ➝ "Black"
    ├── max_speed ➝ 150
    ├── fuel_capacity ➝ 50
    ├── has_sidecar ➝ false
    └── is_sportbike ➝ true
```

#
