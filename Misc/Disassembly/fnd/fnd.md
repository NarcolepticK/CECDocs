# Fnd

- DateTime
  - MAX_DATETIME
  - MIN_DATETIME
  - DateTime()
  - DateToDays()
  - DaysToDate()
  - FromParameters()
  - GetNow()
  - GetParameters()

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
- rootListInitialized
- AppendListObject()
- CreateHeap()
- DestroyHeap()
- FindContainHeap()
- FindListContainHeap()
- GetNextListObject()
- InitFreeMBlock()
- InitHeap()
- InitList()
- InitMBlock()
- NNSi_FndFinalizeHeap()
- NNSi_FndInitHeap()
- RemoveListObject()
- SetFirstObject()