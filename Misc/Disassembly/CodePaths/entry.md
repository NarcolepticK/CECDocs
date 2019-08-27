```
Entry
├── InitRegion
└── InitLocale
    ├── __rt_locale
    └── __get_lc_ctype
        └── strcmp
    └── __get_lc_numeric
        └── strcmp
└── InitSystem
    └── os::Initialize
        └── WaitableCounter::Initialize
           ├── svc::CreateAddressArbiter
           └── SaveThreadLocalRegionAddress
        └── InitializeSharedMemory
            └── InitializeAddressSpaceManager
                └── CriticalSection::Initialize
        └── InitializeStackMemory
            └── AddressSpaceManager::Initialize
                └── CriticalSection::Initialize
        └── InitializeThreadEnvironment
            ├── ThreadLocalStorage::ClearAllSlots
            └── SetupThreadCppExceptionEnvironment
                ├── Sets default unexpected handler
                ├── Sets default terminate handler
                └── __ARM_exceptions_buffer_init
                    └── malloc
                        └── MemoryManager::Alloc
                            ├── CriticalSection::Enter
                            └── ...
                                ├── ...
                                ├── ...
                                ├── ...
                                └── ...
                            └── CriticalSection::Leave
            └── _fp_init
                └── returns 0x3000000
        └── SetProcessInfo
            └── GetAndSetProcessInfoForCurrentProcess0x14
    └── srv::Initialize
        ├── Initialize variables, and two critical sections
        ├── CriticalSection::Enter
        ├── Check initializeCount and RegisterClient or MAKE_ERROR_CODE
        └── CriticalSection::Leave
└── InitStartup
    └── ...
        ├── ...
        ├── ...
        ├── ...
        ├── ...
    └── ...
        ├── ...
        └── ...
└── __cpp__initialize_aeabi
    └── ...
├── InitCallStaticInitializers
└── MainLoop
    ├── ...
    └── ... InitCecdAndRegister
└── svc::ExitProcess:0x03
```