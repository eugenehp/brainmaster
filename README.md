# brainmaster

Rust library and TUI for BrainMaster EEG amplifiers (Atlantis, Discovery, Freedom) via USB serial.

## Features

- Serial communication with BrainMaster EEG devices
- Support for Atlantis, Discovery, and Freedom models
- Optional TUI (Terminal User Interface) for real-time data visualization

## Installation

```bash
cargo add brainmaster
```

### With TUI support

```bash
cargo add brainmaster --features tui
```

## Usage

```rust
use brainmaster::Device;

fn main() -> Result<(), brainmaster::Error> {
    // Connect to a BrainMaster device
    let device = Device::new("/dev/ttyUSB0")?;
    // ...
    Ok(())
}
```

## Running the TUI

```bash
cargo run --features tui
```

## License

GPL-3.0-only
