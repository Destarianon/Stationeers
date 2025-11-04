Cable networks have an additional concept of "channels."

1. Channels are references that data can be stored to/loaded from that exist on the cable network itself.
2. Channels are shared by all devices referencing the same network, and can be used for communication.
3. There are 8 channels on every cable network.
4. Channels are volatile. Anytime the cable network is modified (changed, removed, added to) or when the world exits/loads all data on the channels is deleted.
5. Channels default to NaN, which is not an error, but is not a number value yet.

```mips
# d0 is device zero, and the :0 refers
# to that device's 0 connection
l r0 d0:0 Channel0
```

```mips
#read all 8 channels with a loop and
#place the values in r0 to r7
move r15 LogicType.Channel0 #LogicType integer
move r14 0 #pointer for indirect referencing
loop:
l rr14 db:0 r15
add r15 r15 1 #next channel
add r14 r14 1 #next register
ble r15 LogicType.Channel7 loop
```