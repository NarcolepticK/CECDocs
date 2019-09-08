# Cec

- sessionHandle
###
- GetChangeStateEventHandle()
- Open()
- OpenAndRead()
- OpenAndWrite()
- ReadData()
- SetData()
- Stop()
- WriteMessageWithHmac()

```
Result GetChangeStateEventHandle(Handle *outHandle) {
  u32 tls;
  Result ret;
  u32 *cmdBuf;
  
  tls = GetTLS();
  cmdBuf = (u32 *)(tls + 0x80);
  ipcMakeHeader(&cmdBuf,0x10,0,0,0);
  ret = SendSyncRequest:0x32(sessionHandle);
  if (-1 < ret) {
    *outHandle = cmdBuf[3];
    ret = cmdBuf[1];
  }
  return ret;
}

Result Open(u32 programId, u32 pathType, u32 openFlag, u32 *fileSizeOut) {
  u32 tls;
  Result ret;
  u32 *cmdBuf;
  
  cmdBuf = (u32 *)openFlag;
  tls = GetTLS();
  cmdBuf = (u32 *)(tls + 0x80);
  ipcMakeHeader(&cmdBuf,1,3,2,0);
  cmdBuf[1] = programId;
  cmdBuf[2] = pathType;
  cmdBuf[3] = openFlag;
  ipcDescCurrentProcessId((u32 *)&cmdBuf,4);
  ret = SendSyncRequest:0x32(sessionHandle);
  if (-1 < ret) {
    *fileSizeOut = cmdBuf[2];
    ret = cmdBuf[1];
  }
  return ret;
}


Result OpenAndRead(u32* param_1, uint param_2, uint *param_3, uint param_4, uint param_5, uint param_6) {
  u32 tls;
  Result ret;
  u32 *cmdBuf;
  
  tls = GetTLS();
  cmdBuf = (u32 *)(tls + 0x80);
  ipcMakeHeader(&cmdBuf,0x12,4,4,0);
  cmdBuf[1] = param_2;
  cmdBuf[2] = param_4;
  cmdBuf[3] = param_5;
  cmdBuf[4] = param_6;
  ipcDescCurrentProcessId((u32 *)&cmdBuf,5);
  FUN_0010f5a4((int *)&cmdBuf,7,param_1,param_2);
  ret = SendSyncRequest:0x32(sessionHandle);
  if (-1 < ret) {
    *param_3 = cmdBuf[2];
    ret = cmdBuf[1];
  }
  return ret;
}

Result OpenAndWrite(u32* param_1, uint param_2, uint param_3, uint param_4, uint param_5) {
  u32 tls;
  Result ret;
  u32 *cmdBuf;
  
  tls = GetTLS();
  cmdBuf = (u32 *)(tls + 0x80);
  ipcMakeHeader(&cmdBuf,0x11,4,4,0);
  cmdBuf[1] = param_2;
  cmdBuf[2] = param_3;
  cmdBuf[3] = param_4;
  cmdBuf[4] = param_5;
  ipcDescCurrentProcessId((u32 *)&cmdBuf,5);
  FUN_0010f5b8((int *)&cmdBuf,7,param_1,param_2);
  ret = SendSyncRequest:0x32(sessionHandle);
  if (-1 < ret) {
    ret = cmdBuf[1];
  }
  return ret;
}

Result ReadData(u32 *destBufferAddress, u32 destBufferSize, u32 infoType, u32 *paramBufferAddress, u32 paramBufferSize) {
  u32 tls;
  Result ret;
  u32 *cmdBuf;
  
  tls = GetTLS();
  cmdBuf = (u32 *)(tls + 0x80);
  ipcMakeHeader(&cmdBuf,10,3,4,0);
  cmdBuf[2] = infoType;
  cmdBuf[3] = paramBufferSize;
  cmdBuf[1] = destBufferSize;
  FUN_0010f5b8((int *)&cmdBuf,4,paramBufferAddress,paramBufferSize);
  FUN_0010f5a4((int *)&cmdBuf,6,destBufferAddress,destBufferSize);
  ret = SendSyncRequest:0x32(sessionHandle);
  if (-1 < ret) {
    ret = cmdBuf[1];
  }
  return ret;
}

Result SetData(u32 programId, u32 *bufferAddress, u32 bufferSize, u32 option) {
  u32 tls;
  Result ret;
  u32 *cmdBuf;
  
  cmdBuf = (u32 *)bufferSize;
  tls = GetTLS();
  cmdBuf = (u32 *)(tls + 0x80);
  ipcMakeHeader(&cmdBuf,9,3,2,0);
  cmdBuf[3] = option;
  cmdBuf[1] = programId;
  cmdBuf[2] = bufferSize;
  FUN_0010f5b8((int *)&cmdBuf,4,bufferAddress,bufferSize);
  ret = SendSyncRequest:0x32(sessionHandle);
  if (-1 < ret) {
    ret = cmdBuf[1];
  }
  return ret;
}

Result Stop(CecCommand command) {
  u32 tls;
  Result ret;
  u32 *cmdBuf;
  
  tls = GetTLS();
  cmdBuf = (u32 *)(tls + 0x80);
  ipcMakeHeader(&cmdBuf,0xc,1,0,0);
  cmdBuf[1] = command;
  ret = SendSyncRequest:0x32(sessionHandle);
  if (-1 < ret) {
    ret = cmdBuf[1];
  }
  return ret;
}

Result WriteMessageWithHmac(u32 programId, bool isOutbox, u32 *messageIdBuffer, u32 messageIdSize,
                            u32 *bufferAddress, u32 bufferSize, u32 *hmacKeyAddress) {
  u32 tls;
  Result ret;
  u32 *cmdBuf;

  tls = GetTLS();
  cmdBuf = (u32 *)(tls + 0x80);
  ipcMakeHeader(&cmdBuf,7,4,6,0);
  cmdBuf[1] = programId;
  cmdBuf[2] = isOutbox;
  cmdBuf[4] = bufferSize;
  cmdBuf[3] = messageIdSize;
  FUN_0010f5b8((int *)&cmdBuf,5,bufferAddress,bufferSize);
  FUN_0010f5b8((int *)&cmdBuf,7,hmacKeyAddress,0x20);
  FUN_0010ce86((int *)&cmdBuf,9,messageIdBuffer,messageIdSize);
  ret = SendSyncRequest:0x32(sessionHandle);
  if (-1 < ret) {
  ret = cmdBuf[1];
  }
  return ret;
}
```