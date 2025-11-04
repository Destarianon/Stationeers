A register can be referred to by using another register as a pointer. Adding an additional 'r' to a register name uses it as a reference.

Note: The value in the register must be between 0 and 15.

```mips
move r0 5 # stores the value 5 in r0
move rr0 10 
# is now the same as 'move r5 10' 
# since r0 has the value 5, rr0 points at the register r5
```

Additional r's can be added to do indirect referencing multiple times in a row.

```mips
move r1 2
move r2 3
move rrr1 4
# is now the same as 'move r3 4'
# since r1 points at r2 which points at r3
```

This also works with devices

```mips
move r0 2 # stores the value 2 in r0
s dr0 On 1 
# is now the same as 's d2 On 1'
# r0 has the value 2 so dr0 points at d2
```