# CecMBoxInfoHeader

    u16 magic; // 0x6363 'cc'
    u16 padding1;
    u32 programId;
    u32 privateId;
    u8 flag;
    u8 flag2;
    u16 padding2;
    u8 hmacKey[32];
    u32 padding3;
    CecTimestamp lastAccessed;
    u32 padding4;
    CecTimestamp lastReceived;
    u32 padding5;
    CecTimestamp unknownTime;