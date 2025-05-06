# monokakido.rs
A Rust library for parsing and interpreting the [Monokakido](https://www.monokakido.jp/en/dictionaries/app/) dictionary format.
Aiming for full test coverage and efficient implementation with minimal dependencies.


## usage:
This must be used as a library, rather than a program, so for parsing the actual dictionaries, you should use [this cli](https://git.ajattix.org/hashirama/mkd-utils)<br></br>
In linux (or any other unix):
```shell
$ ./target/release/mkd-utils -e -o le_output/ scan-dict ../Monokakido\ Dictionaries/Portugues/
```
another example with another dictionary:
```shell
$ ./target/release/mkd-utils -e -o le_output/ scan-dict ../Monokakido\ Dictionaries/Portugues/KANKENKJ2/
```
the output will be a folder with xml files, which are human-readable, and a simple script can parse it: 

<img src="https://github.com/user-attachments/assets/d614631b-794e-4914-aeef-226f25eb90cc" width="40%" />


## Notice

This library started as a personal project driven by curiosity.
It is ABSOLUTELY NOT inteded to support piracy;
I strongly condemn making unauthorized copies of Monokakido's dictionaries,
and take no part or responsibility in that kind of activity.
Please buy your own dictionaries directly from Monokakido to show your love and support.

## TODO:
- Add headline support
- Refactor as a workspace to separate the dependencies of the library and the binaries
- Move to mmap-based indexes
- Add graphics support
- Add TTY detection to CLI (prevent binary output to shell)
- Add proper argument parser lib to CLI
- Refine CLI according to the plan below
- Document the rsc, nrsc and keystore and headline formats
### Test:
- Audio using "rsc" (CCCAD, WISDOM3)
- Audio using "nrsc" (DAIJISEN2, NHKACCENT2, OALD10, OLDAE, OLEX, OLT, RHEJ, SMK8)
- Multiple contents (WISDOM3, OLEX)


## CLI　（Planned）

### Tab-separated output formats:
- keyword
- headline
- iid (item id)
- pid (page id)
- aid (audio id)
- gid (graphics id)

### \n\n separated output formats:
- item
- page

### binary output formats:
- audio
- graphics


## Planned to support:
- WISDOM3
- SMK8
- NHKACCENT2
- DAIJISEN2
