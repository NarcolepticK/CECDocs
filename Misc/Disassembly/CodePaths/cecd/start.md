# Start
```
Result Start(CecCommand command)
{
  Result res;
  Result res2;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::Start(command);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res2 = cecd::u::Start(command);
    return res2;
  }
  return 0xE0810BF8;
}
```