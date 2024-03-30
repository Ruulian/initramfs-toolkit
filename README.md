# initramfs-toolkit

## Description

[initrafms-toolkit](https://github.com/Ruulian/initramfs-toolkit) is a toolkit that allows to extract and compress initramfs cpio, useful for Linux kernel exploitation.

Here is the list of the available compression systems:
- gzip
- bzip2
- lz4
- lzma
- lzop
- xz
- zstd

You can also use the tool to compress/extract cpio without any compression system.

## Usage

### extract-initramfs

The usage for this tool is very basic, here is the help page:

```
env@Ruulian:~$ ./extract-initramfs -h
Usage: ./extract-initramfs initrd/initramfs [-o output_directory] [-f]
Options:
  -o : Specify the output directory (default: 'initrd-root')
  -f : Force creation of output (overwritten if already existing)
  -h : Print this help message
```

**Note**: This tool also allows to extract concatenated cpios in one archive

### compress-initramfs

TODO

## Setup

To use this toolkik, the following packages are needed:

```
cpio gzip bzip2 xz-utils zstd lz4 lzop
```

## Contribution

Pull requests are welcome. Feel free to open an issue if you encounter any problem or want to add any feature.