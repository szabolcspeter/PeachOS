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
make
qemu-system-x86_64 -hda ./bin/boot.bin
```

### clean:
```
make clean
```

### current status:
| Task                              | Status          |
| --------------------------------- | ----------------|
| Enabling A20 line                 | In progress     |

### completed tasks:
- [x] Creating boot sector in 16 bits real mode
- [x] Entering 32 bits protected mode
