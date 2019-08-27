# ReadData
```
Result ReadData(u32 destBufferSize, u32 infoType, u32 paramBufferSize, u32 *paramBufferAddress,
                u32 *destBufferAddress)
{
  Result res;
  Result res2;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::ReadData(destBufferSize, infoType, paramBufferSize, paramBufferAddress, destBufferAddress);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res2 = cecd::u::ReadData(destBufferSize, infoType, paramBufferSize, paramBufferAddress, destBufferAddress);
    return res2;
  }
  return 0xE0810BF8;
}
```