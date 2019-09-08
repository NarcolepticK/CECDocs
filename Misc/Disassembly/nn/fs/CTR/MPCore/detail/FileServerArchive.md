# FileServerArchive

- pOpenFile
- sArchiveHeap
- sDirectoryHeap
- sFileHeap
- sFileServerDirectoryBuffer
- sFileServerFileBuffer
###
- CreateDirectory()
- DeleteDirectory()
- DeleteDirectoryRecursively()
- DeleteFile()
- DeleteObject()
- GetIpcObject()
- OpenDirectory()
- OpenFile()
- ~FileServerArchive()
###
- Directory
  - Close()
  - DeleteObject()
  - GetHandle()
  - TryRead()
  - ~Directory()
###
- File
  - Close()
  - File()
  - GetHandle()
  - TryGetSize()
  - TryRead()
  - TrySetSize()
  - TryWrite()
  - ~File()