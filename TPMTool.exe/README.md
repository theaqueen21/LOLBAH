# Proxying Command Execution By Utilizing TPMTool.exe
>Shoutout And Credit Goes To [Grzegorz Tworek] For Tweeting This LOLB

TPMTool.exe Utility Can Retrieve Information About The TPM Module

Playing Around With The Utility
```shell
tpmtool.exe drivertracing stop
```

Looking For Any Weird Behavior In ProcMon, It Is Seen That tpmtool.exe Spawns A Child Process Of cmd.exe

![2](https://user-images.githubusercontent.com/94680549/228516637-ff1931a2-0266-45bc-a5b1-c413deaeaa94.png)

Inclusing cmd.exe Process Name As A Filter, It Is Seen That cmd.exe Makes Use Of Another Windows Utility Called logman.exe

![3](https://user-images.githubusercontent.com/94680549/228520122-7ee024ff-5272-4a33-bc31-7f73f0f7defc.png)

In The Event Properties It Is Seen That A Directory Is Not Specified When Running logman.exe, So It Is Clear That We Can Run Our Own logman.exe In The Current Directory

As An Example Copy C:\Windows\System32\calc.exe To The Current Directory, Rename It To logman.exe And Run The Same Command As Before

```shell
copy C:\Windows\System32\calc.exe .
```

![4](https://user-images.githubusercontent.com/94680549/228521113-9b374cfc-cc22-4ea0-b933-c990f6f7c997.png)

```shell
ren calc.exe logman.exe
```

![5](https://user-images.githubusercontent.com/94680549/228521153-421c23de-84ac-4dee-93d4-cf5d5897dc7e.png)

```shell
tpmltool.exe drivertracing stop
```

![6](https://user-images.githubusercontent.com/94680549/228522481-7ee351d1-6f90-40cb-9496-d3da99a2374e.png)

As You Can See The Process Is Successful But Instead Of Opening The logman.exe Utility The Calculator Is Opened


Instead Of The Calculator You Can Make Use Of Malware Or Other Windows Utilities To Create Weird Or Malicious Behavior


>Note: In The System Logs Nothing Out Of The Ordinary Is Present Which Makes Analysis For The SysAdmin Or The Blue Team Members Harder

![7](https://user-images.githubusercontent.com/94680549/228524393-da8affc6-b405-4bc7-bddd-6ec7b1a289a0.png)


[Grzegorz Tworek]: https://twitter.com/0gtweet







