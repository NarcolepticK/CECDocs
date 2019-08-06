# ReadData

### Inputs:
    0 : Header Code[0x000A00C4]
    1 : Destination buffer size (unused)
    2 : Info type
    3 : Param buffer size (unused)
    4 : Descriptor for mapping a read-only buffer in the target process
    5 : Param buffer address
    6 : Descriptor for mapping a write-only buffer in the target process
    7 : Destination buffer address
### Outputs:
    1 : Result of function, 0 on success, otherwise error code
    2 : Descriptor for mapping a read-only buffer in the target process
    3 : Param buffer address
    4 : Descriptor for mapping a write-only buffer in the target process
    5 : Destination buffer address