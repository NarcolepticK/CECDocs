# ReadMessage

### Inputs:
    0 : Header Code[0x00030104]
    1 : NCCH Program ID
    2 : bool is_outbox
    3 : Message ID size (unused, always 8)
    4 : Buffer size (unused)
    5 : Descriptor for mapping a read-only buffer in the target process
    6 : Message ID address
    7 : Descriptor for mapping a write-only buffer in the target process
    8 : Buffer address
### Outputs:
    1 : Result of function, 0 on success, otherwise error code
    2 : Read size
    3 : Descriptor for mapping a read-only buffer in the target process
    4 : Message ID address
    5 : Descriptor for mapping a write-only buffer in the target process
    6 : Buffer address