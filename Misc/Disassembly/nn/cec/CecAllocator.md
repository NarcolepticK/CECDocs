# CecAllocator

- allocatedCount
- pAllocateFunction
- pAllocator
- vtable

- Allocate()
- Free()
- SetAllocatorPointer()
- ~CecAllocator()

```
void SetAllocatorPointer(void) {
  pAllocator = GetAllocator();
  return;
}

void ~CecAllocator(void) {
  return;
}
```