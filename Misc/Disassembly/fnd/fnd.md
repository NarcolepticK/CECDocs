# Fnd

- ExpHeapBase
  - vtable
  - Finalize()
  - ~ExpHeapBase()

- `ExpHeapTemplate<os::LockPolicy::NoLock>`
  - vtable
  - ~ExpHeapTemplate()

- HeapBase
  - vtable
  - ~HeapBase()

- IAllocator

- UnitHeapBase
  - vtable
  - Initialize()

- `UnitHeapTemplate<os::LockPolicy::Object<os::CriticalSection>>`
  - vtable
  - UnitHeapTemplate()
  - ~UnitHeapTemplate()


### ::detail
- sRootList
- DestroyHeap()
- FindContainHeap()
- GetNextListObject()
- NNSi_FndFinalizeHeap()
- RemoveListObject()