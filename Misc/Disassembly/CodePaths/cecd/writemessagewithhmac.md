# Start
```
Result WriteMessageWithHMAC(programId, isOutbox, messageIdSize, bufferSize,
                            bufferAddress, hmacKeyAddress, messageIdAddress)
{
  Result res;
  Result res2;
  
  if (cecd::s::sessionHandle != 0) {
    res = cecd::s::WriteMessageWithHMAC(programId, isOutbox, messageIdSize, bufferSize,
                                        bufferAddress, hmacKeyAddress, messageIdAddress);
    return res;
  }
  if (cecd::u::sessionHandle != 0) {
    res2 = cecd::u::WriteMessageWithHMAC(programId, isOutbox, messageIdSize, bufferSize,
                                         bufferAddress, hmacKeyAddress, messageIdAddress);
    return res2;
  }
  return 0xE0810BF8;
}
```