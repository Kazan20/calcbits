
# calcbits

`calcbits` is a Rust library for **bit-level calculations and analysis**.  
It provides simple and efficient utilities to manipulate, inspect, and compute values at the bit level.

---

## ✨ Features
- Count the number of set/unset bits in integers.
- Perform bitwise operations with convenience functions.
- Convert between binary/hexadecimal/string forms.
- Useful for algorithms, cryptography experiments, compression, and systems programming.

---

## 📦 Installation

Add `calcbits` to your project with Cargo:

```toml
[dependencies]
calcbits = "0.1.0"
````

Then import it in your code:

```rust
use calcbits::bits;
```

---

## 🚀 Examples

```rust
use calcbits::bits;

fn main() {
    let n: u32 = 0b101101;

    // Count set bits
    let count = bits::count_ones(n);
    println!("Set bits: {}", count); // → 4

    // Count unset bits
    let zeros = bits::count_zeros(n);
    println!("Unset bits: {}", zeros);

    // Convert to binary string
    println!("Binary: {}", bits::to_binary_string(n, 8)); // → "00101101"

    // Bit masking
    let masked = bits::mask(n, 0b1111);
    println!("Masked: {:b}", masked); // → "1101"
}
```

---

## 📖 API Overview

* `count_ones(x)` → number of set bits in `x`
* `count_zeros(x)` → number of unset bits in `x`
* `to_binary_string(x, width)` → binary representation padded to `width`
* `mask(x, mask)` → apply a mask
* More functions coming soon!

---

## 🛠 Development

Clone the repo and run tests:

```sh
git clone https://github.com/yourname/calcbits
cd calcbits
cargo test
```

---

## 📜 License

Licensed under either of:

* MIT License ([LICENSE-MIT](LICENSE-MIT) or [http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT))

---

Made with ❤️ in Rust.