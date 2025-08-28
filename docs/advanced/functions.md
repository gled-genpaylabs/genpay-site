# Functions

**Genpay** allows you to define your own functions with different properties. <br/>
_Note that_ public functions is used for including from other modules.

## Syntax
_Definition Syntax:_
```genpay
pub/NOTHING fn identifier ( param: type, ... ) type/NOTHING {
  // CODE
}
```

_Usage Syntax_
```genpay
identifier ( param, ... )
```

## Examples
```genpay
fn greet(name: *char) *char {
  return format!("Hello, {}!", name);
}

fn main() i32 {
  println!("{}", greet("Genpay"));
  return 0;
}
```
```
Hello, Genpay!
```

----

```genpay
// lib.genpay
pub fn PI() f64 {
  return 3.141592
}

// main.genpay
include "lib.dn"

fn main() {
  println!("PI = {}", PI());
}
```
```
3.141592
```
