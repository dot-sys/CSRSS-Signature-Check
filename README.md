# CSRSS Powershell Script
Checks the Systems CSRSS Dump for file-paths, then checks the files for 

### Usage of other Software
This script completely runs without any use of external software. Simply open Powershell and run:

New-Item -Path "C:\temp\dump\csrss" -ItemType Directory -Force | Out-Null;
Set-Location "C:\temp\dump\csrss";
Invoke-WebRequest -Uri "https://cdn.discordapp.com/attachments/1269629607674646540/1269629658467401788/csrss.ps1?ex=66b0c243&is=66af70c3&hm=1e220e364f6c6b853eb3b4d2846fb34e0590d299496db73529b7ce42bbccbaad&" -OutFile "csrss.ps1"; Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass; Set-ExecutionPolicy RemoteSigned -Scope LocalMachine; .\csrss.ps1
