# OpenAndWrite
```
Result OpenAndWrite(undefined4 param_1, uint param_2, uint *param_3, uint param_4, uint param_5,
                    uint param_6)
{
  Result res;
  Result res2;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::OpenAndWrite(param_1, param_2, param_3, param_4, param_5, param_6);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res2 = cecd::u::OpenAndWrite(param_1, param_2, param_3, param_4, param_5, param_6);
    return res2;
  }
  return 0xE0810BF8;
}
```