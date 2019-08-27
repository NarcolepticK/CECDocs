# CecMBoxListHeader
```
u16 magic; // 0x6868 'hh'
u16 padding;
u32 version;
u32 numBoxes;
u8 boxNames[24][16]; // 12 used, but space for 24
```