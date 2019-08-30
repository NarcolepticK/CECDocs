# LightEvent

### Initialize
```
SimpleLock::Initialize(this->lock)
if (isSomething == false) {
    value = -1
} else {
    value = -2
}
SetState(this, value)
return
```

### SetState
```
s32 val = value
Swap(this, &val)
return
```

### Signal
```
if (this->state != -1) {
  if (this->state == -2) {
    SimpleLock::Lock(&this->lock)
    SetState(this,1)
    WaitableCounter::ArbitrateAddress:Signal(this,-1)
    SimpleLock::Unlock(&this->lock)
  }
  return
}
SetState(this,0)
WaitableCounter::ArbitrateAddress:Signal(this,1)
return
```

### ClearSignal
```
if (this->state != 1) {
  if (state == 0) {
    SetState(this,-1)
  }
  return
}
SimpleLock::Lock(&this->lock)
SetState(this,-2)
SimpleLock::Unlock(&this->lock)
return
```

