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

#### remote debugging:
```
cd bin
add-symbol-file ../build/kernelfull.o 0x100000
y
break _start
target remote| qemu-system-x86_64 -hda ./os.bin -S -gdb stdio
c
layout asm
stepi
```

### clean:
```
make clean
```

### current status:
| Task                              | Status          |
| --------------------------------- | ----------------|
| Implementing PIC                  | In Progress     |

### completed tasks:
- [x] Creating boot sector in 16 bits real mode
- [x] Entering 32 bits protected mode
- [x] Enabling A20 line
- [x] Creating C Cross Compiler (gcc)
- [x] Loading kernel into memory (1M), remote debugging with symbols
- [x] Basic C print functions for writing to the screen
- [x] Interrupt Descriptor Table
