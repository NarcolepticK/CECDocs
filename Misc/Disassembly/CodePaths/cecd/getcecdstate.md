# GetChangeStateEventHandle
```
Result GetCecdState(void)
{
  Result res;
  Result res2;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::GetCecdState(void);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res2 = cecd::u::GetCecdState(void);
    return res2;
  }
  return 0xE0810BF8;
}
```