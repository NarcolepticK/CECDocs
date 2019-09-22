# GetChangeStateEventHandle
```
Result GetChangeStateEventHandle(eventHandle)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::GetChangeStateEventHandle(eventHandle);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::GetChangeStateEventHandle(eventHandle);
    return res;
  }
  return 0xE0810BF8;
}
```
