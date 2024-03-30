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
  -f : Force creation of output directory (overwrite if already exists)
  -h : Print this help message
```

**Note**: This tool allows by default to extract cpios concatenated in one archive

### compress-initramfs

```
env@Ruulian:~$ ./compress-initramfs -h
Usage: ./compress-initramfs compression_type input_directory [-o output_filename]

Compression type:
You can choose among the following types: [ lzma lz4 xz cpio zstd gzip bzip2 lzop ]

Input directory:
Choose the directory fs to archive

Options:
  -o : Specify output file name
  -h : Print this help message
```

## Setup

To use this toolkit, the following packages are needed:

```
cpio gzip bzip2 xz-utils zstd lz4 lzop
```

## Contribution

Pull requests are welcome. Feel free to open an issue if you encounter any problem or want to add any feature.