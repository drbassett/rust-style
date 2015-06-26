# Functions

## Signature Formatting

Functions signatures are divided into several parts: the function name, the generic type list, the parameter list, the return type, and the where clause. The following paragraphs cover the formatting guidelines for each of these individual sections.

The Rust compiler is adamant about using snake case (i.e. `my_function_name`) function names, so this is the recommendend naming convention. Not much more to say about those.

The generic type list immediately follows the function name, and is surrounded by the `<` and `>` characters. There should be no space preceding the opening `<` and no space following the closing `>`. The generic type list contains both lifetimes and generic types. These are separated by commas. After each comma, there should be exactly one space. Generic type names should be preceded by a capital `T`, and then a descriptive name. Avoid single-letter generic type names, as are often popular in this case. Generic types are permitted to specify constraints in this list by following the generic's name with a colon, and then the constraints, separated by a `+`. There should be exactly one space on each side of the colon, and exactly one space around each of the commas.

Immediately following the generic type list is the parameter list, which is surrounded by a pair of parantheses. There should be no space preceding or following the opening parenthesis. Within the parentheses, each parameter is specified with a name, followed by a colon, followed by a type. There should be exactly one space preceding and following this colon. Between each parameter is a comma. There should be no space preceding this comma, and exactly one space following this comma.

Following the parameter list is the return type. These are pretty cut and dry - simply include exactly one space before and after the return arrow `->`, and then write the return type.

Finally, some functions have where clauses. The `where` keyword should be preceded and followed by exactly one space. Within the where clause, the the same syntax is used as within the generic type list. Since style guides are boring enough as it is, I won't bother reiterating those here.

Ok, I lied - there is one more thing. The opening curly brace for the function body should go on the same line as the function, not the next line. There should be exactly one space preceding it.

**TLDR: Here are what your function signatures should look like:**

Just a return type:
``` rust
fn my_function_name() -> ReturnType {
    // ...
}
```

With generic type list:
``` rust
fn my_fun<'a, 'b', TGeneric1 : Constaint1 + Constraint2>() {
    // ...
}
```

With parameters:
``` rust
fn my_fun(param1 : Type1, param2 : Type2) {
    // ...
}
```

With where clause:
``` rust
fn my_fun<TGeneric1, TGeneric2>() where TGeneric1 : Constaint1, TGeneric2 : Constraint2 {
    // ...
}
```
