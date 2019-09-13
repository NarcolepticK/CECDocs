# Cec

- ::CTR
  - ::anon
    - pAllocatorFunction
    - pAllocator
  - CecAllocator
  - CecControl
  - CecControlSys
  - ::detail
    - ::anon
      - PORT_NAME_CEC
      - PORT_NAME_CEC_SYS
      - PORT_NAME_CEC_NDM
    - Cec
    - CecNdm
    - CecSys
    ###
    - GetCecdState()
    - GetChangeStateEventHandle()
    - Open()
    - OpenAndRead()
    - OpenAndWrite()
    - ReadData()
    - SetData()
    - Start()
    - Stop()
    - WriteMessageWithHmac()
  ###
  - Message
  - MessageBox
  - MessageId
  ###
  - os_free()
  - os_malloc()
  - SetAllocFunc()
  ###
  - s_NotificationHandler:0x100
  - s_NotificationHandler:0x105
  - s_NotificationHandler:0x106