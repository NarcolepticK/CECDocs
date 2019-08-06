# Read

### Inputs:
    0 : Header Code[0x00020042]
    1 : Buffer size (unused)
    2 : Descriptor for mapping a write-only buffer in the target process
    3 : Buffer address
### Outputs:
    1 : Result of function, 0 on success, otherwise error code
    2 : Read size
    3 : Descriptor for mapping a write-only buffer in the target process
    4 : Buffer address