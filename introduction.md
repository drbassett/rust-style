# The Basics
The accepted term for a rust developer is `rustacean`. Acceptable prompts for developing Rust code include:
> Feeling rusty?

> Wanna get rustified?

## A well-formed example
``` rust
use std::io;

fn main() {
	println!("Hello, world!");
}
```

## Naming
* Use `snake_case` for `fn` names, variable names, and module names
* Use `UpperCamelCase` for `trait`s, `struct`s, `enum`s, and `enum` variants
* Use single, lowercase characters for lifetime names e.g. `'a` or `'b`

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

