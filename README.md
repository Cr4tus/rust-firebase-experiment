# Rust Firebase Experiment

## What does the app do?
The program simply creates a firebase instance that inserts an object of type: *User* via specialized repository

## Programming Languages:
- Rust

## Frameworks & Libraries:
- firebase-rs - https://crates.io/crates/firebase-rs/2.0.6/dependencies | https://docs.rs/firebase-rs/latest/firebase_rs/struct.Firebase.html
- serde - https://serde.rs | https://docs.rs/serde/latest/serde/
- serde-json - https://docs.rs/serde_json/latest/serde_json/
- tokio - https://tokio.rs | https://docs.rs/tokio/latest/tokio/

## Implementation:
The app has 4 modules:
- data (*data.rs* - containing the *User* entity)
```rust
pub mod entity {
    use serde::{Serialize, Deserialize};

    #[derive(Serialize, Deserialize, Debug)]
    pub struct User {
        pub name: String,
        pub email: String,
        pub age: u32
    }
}
```
- repo (*repo.rs* - containing the *Repo* that handles the users insertion)
- utils (*utils.rs* - containing the deserialization utils)