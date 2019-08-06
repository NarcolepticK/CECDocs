# WriteMessage

### Inputs:
    0 : Header Code[0x00060104]
    1 : NCCH Program ID
    2 : bool is_outbox
    3 : Message ID size(unused, always 8)
    4 : Buffer size(unused)
    5 : Descriptor for mapping a read-only buffer in the target process
    6 : Buffer address
    7 : Descriptor for mapping a read/write buffer in the target process
    8 : Message ID address
### Outputs:
    1 : Result of function, 0 on success, otherwise error code
    2 : Descriptor for mapping a read-only buffer in the target process
    3 : Buffer address
    4 : Descriptor for mapping a read/write buffer in the target process
    5 : Message ID address