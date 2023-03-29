# Proxying Command Execution By Utilizing TPMTool.exe

TPMTool.exe Utility Can Retrieve Information About The TPM Module

Playing Around With The Utility
```shell
tpmtool.exe drivertracing stop
```
Looking For Any Weird Behavior In ProcMon, It Is Seen That tpmtool.exe Spawns A Child Process Of cmd.exe



