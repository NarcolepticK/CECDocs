# SimpleLock

### Initialize
```
s32 val = 1
Swap(this->lock, &val)
return
```

### Lock
```
bool lockAcquired = TryLock()
if (lockAcquired == false) {
    impl::Lock()
}
return
```

### TryLock
```
bool lockAcquired = impl::TryLock()
return lockAcquired
```

### Unlock
```
s32 val
impl::Unlock(this, &val)
if (1 < val) {
    WaitableCounter::ArbitrateAddress(this->lock, ARBITRATION_SIGNAL, 1)
}
return
```