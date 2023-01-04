# simpleOS
#### This project follows [Philipp Oppermann's blog](https://os.phil-opp.com/) to build a basic operating system in Rust. simpleOS targets a `x86_64` system and runs on bare metal. With the exception of the BIOS bootloader, for which we use an existing crate, everything is built from scratch. This was a project I decided to take on to dive deeper into understanding what exactly an operating system is and how it works.

## Bare Bones
A minimal 64-bit Rust kernel for x86 architecture is built on a freestanding Rust binary that does not link the standard library so it can run on bare metal for a custom target. After compiling the kernel, it needs to be linked to the bootloader. The `bootloader` crate is used to implement a basic BIOS bootloader. After compiling the kernel and bootloader, the kernel is linked with the bootloader to create a bootable disk image. 
