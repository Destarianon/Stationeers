Like other concepts such as Color and Mode, LogicTypes are a enum which is identified by a unique integer. Because of this, you can use loops or the stack to dynamically refer to a specific LogicType value for a device.

```mips
#loop through a list of LogicTypes
push LogicType.RatioOxygen
push LogicType.RatioVolatiles
push LogicType.Temperature
loop:
pop r1
l r0 myDevice r1
...
bgtz sp loop #loop until the Stack is empty
```