# Nuit Multiplatform Example

A small example for a simple multiplatform (desktop + mobile) app written in Rust using the declarative UI library [Nuit](https://github.com/fwcd/nuit).

> [!IMPORTANT]
> This is highly experimental and currently only works on macOS and iOS. Support for more platforms, especially Linux, is planned in the future.

## Getting Started

First make sure to have [`cargo-mobile2`](https://github.com/tauri-apps/cargo-mobile2) installed, then run

```sh
cargo mobile init
```

> [!NOTE]
> If the `gen` folder already exists, you may have to delete it first due to https://github.com/tauri-apps/cargo-mobile2/issues/351.

To run

- on desktop use `cargo run`
- on iOS use `cargo apple run`
- on Android use `cargo android run`

> [!TIP]
> For iOS and Android you can also open the project in the corresponding IDE with `cargo apple open` (Xcode) and `cargo android open` (Android Studio), respectively.

## Implementation Notes

- The `#[mobile_entry_point]` annotation generates all the boilerplate `extern` functions for mobile.
- Logging on Android is done using `android_logger`.
