# Start
```
Result Start(CecCommand command)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::Start(command);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::Start(command);
    return res;
  }
  return 0xE0810BF8;
}
```
