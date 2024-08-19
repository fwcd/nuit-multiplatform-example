# Nuit Multiplatform Example

A small example for a simple multiplatform (desktop + mobile) app written in Rust using the declarative UI library [Nuit](https://github.com/fwcd/nuit).

> [!IMPORTANT]
> This is highly experimental and currently only works on macOS and iOS. Support for more platforms, especially Linux, is planned in the future.

## Getting Started

First make sure to have [`cargo-mobile`](https://github.com/BrainiumLLC/cargo-mobile) installed, then run

```sh
cargo mobile init
```

To run this on desktop, just do `cargo run` like normal! For mobile, use `cargo android run` and `cargo apple run` respectively (or use `cargo android open` and `cargo apple open` to open in Android Studio and Xcode respectively).

- The `#[mobile_entry_point]` annotation generates all the boilerplate `extern` functions for mobile.
- Logging on Android is done using `android_logger`.
