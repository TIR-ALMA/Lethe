# Lethe
This is a Ransomware/Trojan. Its objective is to infiltrate the system, blur all photos and videos (making them irrecoverable), delete them, and replace them with the blurred versions.
It is essentially a hybrid of file-based and fileless malware, meaning it operates both in RAM (memory) and on the storage drive simultaneously.

It utilizes:

1. D/Invoke (Dynamic Invocation): Calls WinAPI functions by dynamically resolving their addresses instead of standard linking. This complicates static analysis and signature detection.
2. In-Memory Execution: File processing and shellcode execution occur in memory, avoiding writing intermediate files to disk.
3. Introspection/JIT Execution: Executes dynamically placed machine code (shellcode) through JIT compilation.
4. PowerShell: Executes commands via built-in PowerShell, which can be less noticeable than typical processes.

It is offtoned, meaning it operates without a Command and Control (C2) server.
