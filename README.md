# Trotline

This is just a project I'm using to learn concurrency and file IO in Rust; it isn't fit for any real-world use. If you're looking for a genuinely very useful grep alternative, try [ripgrep][ripgrep], a genuinely very impressive and generally faster search tool also written in Rust.

Trotline creates a new thread for every file being searched then uses regex to identify and print to stdout every line containing the desired pattern. All binary files are ignored.

## Installation

To install, ensure you have the requirements listed below, then run:
```bash
cargo install --git "https://github.com/SuedeGently/trotline.git"
```
then `trotline --version` to check its installed correctly.

### Requirements

* The rust toolchain (rustup, cargo)

## Usage

```
    trotline [FLAGS] <pattern> [directory]

FLAGS:
    -h, --help           Prints help information
    -i, --ignore_case    ignore case
    -V, --version        Prints version information

ARGS:
    <pattern>      regex search pattern
    <directory>    target directory
```

Where `pattern` can be any valid regex string. If no directory is specified, the current working directory will be used instead.


[ripgrep]: https://github.com/BurntSushi/ripgrep
