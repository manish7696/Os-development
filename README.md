# deving os

## started reading a book os dev ::
```
https://littleosbook.github.io/
```

- code in day1 files
- used the following commands to compile the code and verify in qemu

for making executable file:
```
nasm -f elf32 loader.s
ld -T link.ld -melf_i386 loader.o -o kernel.elf
```

for running it and checking contents of eax register:
```
qemu-system-i386 -kernel kernel.elf
gdb -ex "target remote :1234" -ex "symbol-file kernel.elf"
```
