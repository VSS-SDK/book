# Enums

## C++
Domain/TeamType.h
```cpp
namespace vss {
    enum TeamType{
        Yellow = 0,
        Blue = 1
    };     
}
```

Domain/FieldTransformationType.h
```cpp
namespace vss {
    enum FieldTransformationType{
        None = 0,
        Flip180Degrees = 1
    };
}
```

## Rust
domain::team_type::TeamType
```rust
#[derive(Clone, Debug)]
pub enum TeamType {
    Yellow,
    Blue
}
```

use domain::field_transformation_type::FieldTransformationType
```rust
#[derive(Clone, Debug)]
pub enum FieldTransformationType {
    None,
    Flip180Degrees
}
```