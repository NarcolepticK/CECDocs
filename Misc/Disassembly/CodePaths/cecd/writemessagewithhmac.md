# WriteMessageWithHmac
```
Result WriteMessageWithHmac(programId, isOutBox, msgId, msgIdSize, writeBuf, writeBufSize, hmacKey)
{
  Result res;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::WriteMessageWithHmac(programId, isOutBox, msgId, msgIdSize, writeBuf, writeBufSize, hmacKey);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res = cecd::u::WriteMessageWithHmac(programId, isOutBox, msgId, msgIdSize, writeBuf, writeBufSize, hmacKey);
    return res;
  }
  return 0xE0810BF8;
}
```
