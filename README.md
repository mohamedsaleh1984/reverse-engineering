# Reverse-Engineering
Software Reverse Engineering

Using GDB to disassemble binary file
```
dbg <filename.o>
```
```
info functions
```
```
disassemble <functionName>
```

Using objdump to get more information about the binary

- file format
```
objdump -f <filename.o>
```

- disassemble Obj file
```
objdump -gdSC -M intel <filename.o> > <filename>.d
```
- header content
```
objdump -p <filename.o>
```
- disassemble all sections of the file
```
objdump -D <filename.o>
```
- print the content of all sections
```
objdump -s <filename.o>
```
- Extract Data Segment
```
objdump -s Project1.o > DataSegment.txt
```

RegEx to remove mem address - memory references vtable
```
#\s0x[0-9<> _A-Za-z+]+
```

RegEx tto remove mem address - memory address
```
0x[0-9<> _A-Za-z+]+\s<\+[0-9]+>:
```