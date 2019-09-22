# Open
```
Result Open(programId, pathType, flag, size)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::Open(programId, pathType, flag, size);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::Open(programId, pathType, flag, size);
    return res;
  }
  return 0xE0810BF8;
}
```
