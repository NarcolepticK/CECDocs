# os

- AddressSpaceManager
  - Allocate()
  - Free()
  - Initialize()

- ::ARM
  - pThreadLocalRegion
  - GetThreadLLocalRegionAddress()
  - SetThreadLocalRegionAddress()

- CriticalSection
  - Enter()
  - Initialize()
  - IsOwned()
  - Leave()
  - OwnsLock()
  - ~CriticalSection()

- ::detail
  - InitializeSharedMemory()
  - InitializestackMemory()
  - InitializeThreadEnvironment()
  - InternalErrorHandler()

- Event

- LightEvent
  - ClearSignal()
  - Initialize()
  - SetState()
  - Signal()
  - TryWait()
  - Wait()

- LightSemaphore

- Mutex

- Semaphore

- SharedMemoryBlock
  - Finalize()
  - ~SharedMemoryBlock()

- SimpleLock
  - Initialize()
  - Lock()
  - TryLock()
  - Unlock()

- Thread
  - pAutoStackManager
  - CallDestructorAndExit()
  - ConvertPriority()
  - SetAutoStackManagerAddress()
  - SleepThread()
  - ThreadStart()
  - TryInitializeAndStartImpl()
  - TryInitializeAndStartImplUsingAutoStack()

- ThreadLocalStorage
  - TLSMap
  - CheckIndexInMap()
  - ClearAllSlots()
  - ~ThreadLocalStorage()