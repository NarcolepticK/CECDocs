# GetChangeStateEventHandle
```
Result GetCecdState(state)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::GetCecdState(state);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::GetCecdState(state);
    return res;
  }
  return 0xE0810BF8;
}
```
