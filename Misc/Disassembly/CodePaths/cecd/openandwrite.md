# OpenAndWrite
```
Result OpenAndWrite(writeBuf, writeBufSize, programId, pathType, fileFlag)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::OpenAndWrite(writeBuf, writeBufSize, programId, pathType, fileFlag);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::OpenAndWrite(writeBuf, writeBufSize, programId, pathType, fileFlag);
    return res;
  }
  return 0xE0810BF8;
}
```
