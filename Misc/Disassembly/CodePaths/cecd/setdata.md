# SetData
```
Result SetData(u32 programId, u32 pathType, u32 option, u32 *messageIdAddress)
{
  Result res;
  Result res2;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::SetData(programId, pathType, option, messageIdAddress);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res2 = cecd::u::SetData(programId, pathType, option, messageIdAddress);
    return res2;
  }
  return 0xE0810BF8;
}
```