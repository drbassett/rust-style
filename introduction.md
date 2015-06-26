# The Basics
## A well-formed example
``` rust
use std::io;

fn main() {
	println!("Hello, world!");
}
```

## Naming
* Use `snake_case` for `fn` names
* Use `kebab-case` for variables names
* Use `UpperCamelCase` for `traits` and `structs`

## Bracing
### Follow Stroustrup bracing style
All opening braces should be inline and closing braces should be on their own line.

``` rust
fn main() {
	if (true) {
		println!("Hello, world!");
	} else {
		println!("wtf?");
	}
}
```

## Organization
### Organize `use` statements
Helps to avoid duplicate `use` statements.

### `trait`, `Struct`, and `impl`
``` rust
// trait first
pub trait Tile {
    fn get_piece(&self) -> Option<&Piece>;
}

// struct following trait
pub struct EmptyTile;

// impl for trait
impl Tile for EmptyTile {
    fn get_piece(&self) -> Option<&Piece> {
       Option::None
    }
}

// impl for struct
```

