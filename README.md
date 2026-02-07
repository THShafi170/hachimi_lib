# hachimi_lib

The core Rust implementation of common Hachimi components. Provides tag-aware text wrapping and text processing logic.

## Usage (Rust)

Add this to your `Cargo.toml`:

```toml
[dependencies]
hachimi_lib = { git = "https://github.com/THShafi170/hachimi_lib" }
```

```rust
use hachimi_lib::wrap_text;

let text = "Hello <color=red>world</color>";
let wrapped = wrap_text(text, 20, 1.0);
```

## WebAssembly Build

This crate is designed to be compiled to WebAssembly for use in JavaScript environments.

```bash
wasm-pack build --target web --out-dir ../hachimi_lib_js
```

## Features

- **Tag-Aware**: Correctly handles formatting tags (`<color>`, `<size>`, etc.) during text wrapping.
- **Unicode Support**: Uses `textwrap` and unicode segmentation for accurate line breaks.
- **Performance**: Optimized Rust core for text processing.

## Bindings

- **JavaScript/WASM**: [`hachimi_lib_js`](https://github.com/THShafi170/hachimi_lib_js) (The distribution package for web use).

## License

[MIT](LICENSE)
