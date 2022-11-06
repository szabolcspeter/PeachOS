# PeachOS
I'm gonna create and build a 32 bits multihreaded OS kernel completely from scratch.<br/>
This repo is based on https://www.udemy.com/course/developing-a-multithreaded-kernel-from-scratch/<br/>

*This repo is under active development --- as it requires very much time and effort to complete*

### required tools:
- C compiler (gcc)
- nasm assembler
- gdb debugger
- make
- qemu-system-x86_64

### steps to build and run:
```
./build.sh
qemu-system-x86_64 -hda ./bin/os.bin
```

### clean:
```
make clean
```

### current status:
| Task                              | Status          |
| --------------------------------- | ----------------|
| Alignment issues                  | In Progress     |

### completed tasks:
- [x] Creating boot sector in 16 bits real mode
- [x] Entering 32 bits protected mode
- [x] Enabling A20 line
- [x] Creating C Cross Compiler (gcc)
- [x] Loading kernel into memory (1M), remote debugging with symbols
