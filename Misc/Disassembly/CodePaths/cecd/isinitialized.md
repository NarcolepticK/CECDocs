# IsInitialized
```
bool IsInitialized(void)
{
  bool _isInitialized;
  
  if ((isInitialized != false) || (_isInitialized = IsInitializedSys(), _isInitialized != false)) {
    _isInitialized = true;
  }
  return _isInitialized;
}
```