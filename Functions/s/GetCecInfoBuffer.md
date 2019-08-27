# GetCecInfoBuffer

### Inputs:
    0 : Header Code[0x000D0082]
    1 : Buffer size
    2 : unknown
    3 : Descriptor for mapping a write-only buffer in the target process
    4 : Destination buffer address
### Outputs:
    1 : Result of function, 0 on success, otherwise error code
    2 : Descriptor for mappinga a buffer in the target process
    3 : Destination buffer address