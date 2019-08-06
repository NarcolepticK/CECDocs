# SetData

### Inputs:
    0 : Header Code[0x000900C2]
    1 : NCCH Program ID
    2 : Buffer Size
    3 : Option
    4 : Descriptor for mapping a read-only buffer in the target process
    5 : Buffer address
### Outputs:
    1 : Result of function, 0 on success, otherwise error code
    2 : Descriptor for mapping a read-only buffer in the target process
    3 : Buffer address