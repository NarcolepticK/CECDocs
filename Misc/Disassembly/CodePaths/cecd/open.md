# Open
```
Result Open(u32 programId, u32 pathType, u32 openFlag, u32 *fileSizeOut)
{
  Result res;
  Result res2;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::Open(programId, pathType, openFlag, fileSizeOut);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res2 = cecd::u::Open(programId, pathType, openFlag, fileSizeOut);
    return res2;
  }
  return 0xE0810BF8;
}
```