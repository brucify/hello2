hello2
=====

A Rust application

Build
-----

    $ cargo build
    $ tree .
    ├── Cargo.lock
    ├── Cargo.toml
    ├── README.md
    ├── src
    │   ├── bar.rs
    │   ├── foo.rs
    │   ├── lib.rs
    │   └── main.rs

`lib.rs`:

```rust
pub mod bar;
pub mod foo;
```

`main.rs`:

```rust
use hello2::bar;

fn main() {
    println!("Hello, world!");
    bar::bar();
}
```

`foo.rs`:

```rust
pub fn say_foo() {
    println!("Foo");
}
```

`bar.rs`:

```rust
use crate::foo;

pub fn bar() {
    foo::say_foo();
}
```

Source: https://stackoverflow.com/questions/57756927/rust-modules-confusion-when-there-is-main-rs-and-lib-rs
