# OpenAndRead
```
Result OpenAndRead(readBuf, readBufSize, readSize, programId, pathType, fileFlag)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::OpenAndRead(readBuf, readBufSize, readSize, programId, pathType, fileFlag);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::OpenAndRead(readBuf, readBufSize, readSize, programId, pathType, fileFlag);
    return res;
  }
  return 0xE0810BF8;
}
```
