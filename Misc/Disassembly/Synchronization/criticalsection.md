# Critical Section

### Initialize
```
SimpleLock::Initialize(lock)
threadTag = 0
lockCount = 0
return
```
### Enter
```
if (!OwnsLock()) {
    SimpleLock::Lock(lock)
    tls = GetTLS()
    this->threadTag = tls
}
this->lockCount += 1
return
```

### Leave
```
counter = this->lockCount - 1
this->lockCount = counter
if (counter == 0) {
    this->threadTag = 0
    SimpleLock::Unlock(lock)
}
return
```