# ReadData
```
Result ReadData(destBuf, destBufSize, option, paramBuf, paramBufSize)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::ReadData(destBuf, destBufSize, option, paramBuf, paramBufSize);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::ReadData(destBuf, destBufSize, option, paramBuf, paramBufSize);
    return res;
  }
  return 0xE0810BF8;
}
```
