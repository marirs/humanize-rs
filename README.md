Humanize for Rust
=====================
[![Build Status](https://travis-ci.com/marirs/humanize-rs.svg?branch=master)](https://travis-ci.com/marirs/humanize-rs)

This is a simple crate to humanize bytes or Time into human readable format.

### Requirements

- Rust 1.50+

### Usage
```toml
humanize = { git = "https://github.com/marirs/humanize-rs", branch = "master" }
```

and then,

```rust
use humanize::Humanize;

fn main() {
    let epoch_time = UNIX_EPOCH + Duration::from_secs(1610859829);
    let human_time = String::from("Sun Jan 17 2021, 05:03:49");
    assert_eq!(epoch_time.humanize(), human_time);

    let file_size = 1000_f64;
    assert_eq!(file_size.humanize(), "1 kB");
}
```

---
License: MIT