# Embedded-Rust-HelloWorld
Printing Hello World on qemu for Arm by Rust language

## To Compile
This will compile the project for ARM Cortex-M3
``` bash
export RUSTFLAGS="-C link-arg=-Tlink.x"
cargo build --target thumbv7m-none-eabi
```

## To Run it on Qemu
qemu-system-arm -cpu cortex-m3 -machine lm3s6965evb -nographic -semihosting-config enable=on,target=native -kernel target/thumbv7m-none-eabi/debug/hello-embedded-rust

# For more details and information
visit [Start with Embedded Rust -- AmrDrafts](https://amrdrafts.com/topics/embedded-system/embedded-rust)