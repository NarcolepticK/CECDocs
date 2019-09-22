# Stop
```
Result Stop(CecCommand command)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::Stop(command);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::Stop(command);
    return res;
  }
  return 0xE0810BF8;
}
```
