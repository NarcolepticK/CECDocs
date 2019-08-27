# OpenAndWrite

### Inputs:
    0 : Header Code[0x00110104]
    1 : Buffer size (unused)
    2 : NCCH Program ID
    3 : Path type
    4 : File open flag
    5 : Descriptor for process ID
    6 : Placeholder for process ID
    7 : Descriptor for mapping a read-only buffer in the target process
    8 : Buffer address
### Outputs:
    1 : Result of function, 0 on success, otherwise error code
    2 : Descriptor for mapping a read-only buffer in the target process
    3 : Buffer address