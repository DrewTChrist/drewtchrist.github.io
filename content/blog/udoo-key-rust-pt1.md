+++
title = "Rust on the Udoo Key: Part 1"
description = ""
date = 2023-
+++

# Rust on the Udoo Key: Part 1 (RP2040)

## Introduction

The Udoo Key is a microcontroller development board designed by Udoo that was
launched on Kickstarter in late 2021. The Udoo Key comes equipped with both an 
ESP32 and an RP2040. At the time of the launch, this was of course a big 
draw for those that were already making use of the RP2040. Since then, many
ESP32 + RP2040 dev boards have come to the market. The Rasberry Pi Foundation
also released the Pico W giving the Pico form factor wireless capabilities.

## Getting Started

To get started with this guide you'll need to 
[install Rust](https://www.rust-lang.org/learn/get-started). After Rust has 
been installed on your machine you'll need the target for our particular
architecture.

```shell
rustup target add thumbv6m-none-eabi
```

```shell
cargo install flip-link
```

There are several ways to load your code onto an RP2040. If you intend to load 
your program onto the RP2040 over USB with the UF2 bootloader, then you'll want 
to install elf2uf2-rs.

```shell
cargo install elf2uf2-rs
```

If you have a debug probe/JTAG, or a spare Pico, you can load your program to
the RP2040 over the SWD pins using probe-run.

```shell
cargo install probe-run
```

## Programming the RP2040

### Creating the Project

To begin programming the RP2040 we need to create a new project. An easy way to
do this is to clone the RP2040 project template and start with that.

```shell
git clone https://github.com/rp-rs/rp2040-project-template
cd rp2040-project-template
```

By default, the rp2040 project template includes the `pi-pico` crate.
Since we are not technically using a Pico we'll want to include the 
`rp2040-hal` crate. In the `Cargo.toml` of the project, replace this line

```toml
# Your Cargo.toml may show a different version
rp-pico = "0.7"
```

with these lines.

```toml
# There may be newer versions of rp2040-hal and rp2040-boot2 
# since the time of writing, be sure to check
rp2040-hal = { version="0.8", features=["rt", "critical-section-impl"] }
rp2040-boot2 = "0.2"
```

### Writing the Code
* Program the RP2040 to blink the attached LED

### Loading the Code
* Flash through USB
* Flash through SWD
