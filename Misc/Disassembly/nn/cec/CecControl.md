# CecControl

- criticalSection
- enterExclusiveState
- isDebugMode
- isInitialized
- isNdmSuspended
###
- Ctor()
- IsInitialized()
- StartScanning()
- StopScanning()

```
bool IsInitialized(void) {
  bool _isInitialized;
  
  if ((isInitialized != false) || (_isInitialized = IsInitializedSys(), _isInitialized != false)) {
    _isInitialized = true;
  }
  return _isInitialized;
}

Result StartScanning(bool reset) {
  bool isInitialized;
  bool isInitializedSys;
  Result ret;
  ScopedLock lock;

  ret = 0;
  isInitialized = IsInitialized();
  if (isInitialized == false) {
    return 0xc8a10bf0;
  }

  Enter(&lock);
  if (reset != false) {
    isInitializedSys = IsInitializedSys();
    if (((uint)isInitializedSys | (int)isDebugMode) == 0) {
      ret = 0xc8810bea;
      goto leave&return;
    }
    ret = Start(CEC_COMMAND_RESET_FILTER);
  }
  if (EnterExclusiveState == false) {
    Leave(&lock);
    return 0xc8a10bf0;
  }
  if ((isNdmSuspended != false) && (ret = Resume(Cec), -1 < ret)) {
    isNdmSuspended = false;
  }
leave&return:
  Leave(&lock);
  return ret;
}
```