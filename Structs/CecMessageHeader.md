# CecMessageHeader
```
u16 magic; // 0x6060 ``
u16 padding;
u32 messageSize;
u32 totalHeaderSize;
u32 bodySize;
u32 titleId;
u32 titleId2;
u32 batchId;
u32 unknown_1;
u8 messageId[8];
u32 messageVersion;
u8 messageId2[8];
u8 flags;
u8 sendMethod;
u8 unopened;
u8 newFlag;
u64 senderId;
u64 senderId2;
CecTimestamp sent;
CecTimestamp received;
CecTimestamp created;
u8 sendCount;
u8 forwardCount;
u16 userData;
```