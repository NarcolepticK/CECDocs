# Delete

### Inputs:
    0 : Header Code[0x00080102]
    1 : NCCH Program ID
    2 : Path type
    3 : bool is_outbox
    4 : Message ID size (unused)
    5 : Descriptor for mapping a read-only buffer in the target process
    6 : Message ID address
### Outputs:
    1 : Result of function, 0 on success, otherwise error code
    2 : Descriptor for mapping a read-only buffer in the target process
    3 : Message ID address