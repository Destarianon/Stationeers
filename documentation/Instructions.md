In IC10/MIPS, instructions are generally formatted in the following way:

`opcode` `output` `parameter1` `parameter2` ...etc

If the opcode does not produce an output, that option will be skipped.

Examples:
```mips
# moves the integer 11 into register r0
move r0 11

# then adds 1 to r0 and stores the result back into r0
add r0 r0 1

# pops the next value off the stack into r1
pop r1

# continues execution at the label "loop:"
j loop
```

Here is a list of additional notes regarding instructions available in IC10:

https://stationeers-wiki.com/IC10/instructions