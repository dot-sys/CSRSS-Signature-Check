# CSRSS Powershell Script
Checks the Systems CSRSS Dump for file-paths, then checks the files for signatures to ensure file integrity or detect traces of malware on a system.

### Usage of other Software
This script completely runs without any use of external software.

### Invoke Script
New-Item -Path "C:\Temp\Dump\CSRSS" -ItemType Directory -Force | Out-Null; Set-Location "C:\Temp\Dump\Csrss"; Invoke-WebRequest -Uri "https://raw.githubusercontent.com/dot-sys/CSRSS-Signature-Check/master/csrss.ps1" -OutFile "csrss.ps1"; Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force; Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force; .\csrss.ps1
