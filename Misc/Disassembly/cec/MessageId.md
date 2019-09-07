# MessageId

- GetBinary()
- IsEmpty()
- IsEqual()
- MessageId()

```
bool __thiscall IsEmpty(MessageId *this) {
  uint loopCounter;

  loopCounter = 0;
  do {
    if (this->id[loopCounter] != 0) {
      return false;
    }
    loopCounter = loopCounter + 1;
  } while (loopCounter < 8);
  return true;
}
```