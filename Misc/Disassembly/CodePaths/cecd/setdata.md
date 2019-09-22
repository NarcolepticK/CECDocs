# SetData
```
Result SetData(programId, dataBuf, dataBufSize, option)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::SetData(programId, dataBuf, dataBufSize, option);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::SetData(programId, dataBuf, dataBufSize, option);
    return res;
  }
  return 0xE0810BF8;
}
```
