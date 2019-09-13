# Srv

- ::anon
  - PORT_NAME
  - PORT_NAME_FOR_MANAGER
  - s_CriticalSection
  - s_csInitializeLock
  - s_HandlerManager
  - s_InitializeCount
  - s_IsInitialized
  - s_NotificationDispatcher
  - s_NotificationSemaphore
  - s_Stack
  ###
  - ConnectToAndRegisterClient()
  - Exit()
- ::detail
  - ::Service
    - s_Session
    ###
    - EnableNotification()
    - GetServiceHandle()
    - ReceiveNotification()
    - RegisterClient()
    - RegisterService()
    - Subscribe()
    - UnregisterService()
- `EventNotificationHandlerBase<nn::os::LightEvent>`
  - p_HandleNotification
  - vtable
  ###
  - HandleNotification()
  - ~EventNotificationHandlerBase()
- EnableNotification()
- Exit()
- GetServiceHandle()
- Initialize()
- IsInitialized()
- MAKE_ERROR_CODE()
- ReceiveNotification()
- RegisterNotificationHandler()
- Subscribe()
