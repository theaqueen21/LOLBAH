# Install Rogue Software & Packages Using Winget

> Winget Is A Package Manager Developed By Microsoft For Windows. It Allows Users To Easily Install Applications And Tools From The Command Line Using A YAML Manifest File. It Is Available For Windows 10 Version 1809 And Later And Is Designed To Be Simple And Convenient For Managing Software On Windows Machines.

1. Press The Windows Key And R

```
Win + R
```

2. Type WT Then Press CTRL, Shift And Enter To Open Windows Terminal As Administrator

```
WT
```
```
CTRL + Shift + Enter
```

![1](https://user-images.githubusercontent.com/94680549/236493445-253130cf-53a1-4aa2-9697-ca4f8d81f303.jpg)

![2](https://user-images.githubusercontent.com/94680549/236493489-5008458a-a5aa-4e9a-971c-b2cc979aad9b.jpg)

![3](https://user-images.githubusercontent.com/94680549/236493511-6a294b15-86ed-4c07-9ee7-1375aa83a7be.jpg)

![4](https://user-images.githubusercontent.com/94680549/236493587-75801cce-4d37-4c0c-b888-dc6225e7afdc.jpg)

3. Enter The Command Below To Enable The Option Of Using Local Manifest Files To Download Software And Packages

```
winget settings --enable localmanifestfiles
```

![5](https://user-images.githubusercontent.com/94680549/236494421-2ee0a9d9-04b6-4cd3-9199-3cc99b46e60b.jpg)

4. Create A ManifestFile Named manifest.yml, Similar To The [Example] Provided, But With The Fields Updated To Reflect Your Specific Information. 

[Example]: https://github.com/theaqueen21/LOLBAH/blob/main/Winget.exe/manifest.yml

5. Enter The Command Below To Download And Run/Install The Rogue Software Or Package

> Note: The Command Will Not Work If The SHA256 Hash Of The exe Is Invalid Or The manifest.yml File Is In Another Directory

```
winget install --manifest manifest.yml
```

> Note: To Get The SHA256 Hash Of The Installer Run The Command "sha256sum {filename}" In Linux Terminal Or The Command "Get-FileHash -Algorithm SHA256 {filename}" In Windows Powershell

![10](https://user-images.githubusercontent.com/94680549/236503180-bb93db77-8388-40e4-80b7-d62d17f0cbe7.jpg)

![9](https://user-images.githubusercontent.com/94680549/236502180-da2c87a2-3caf-4160-8167-bcb7973c9d65.jpg)

> Note: To Access The Logs Run The Command "winget --info" And Go To The Directory Mentioned

![6](https://user-images.githubusercontent.com/94680549/236499791-29b7c735-a1c6-4ade-aed4-0a3627a0d525.jpg)

![7](https://user-images.githubusercontent.com/94680549/236500368-ed44aea5-39c4-447e-80f5-b0e92f3f9317.jpg)

![8](https://user-images.githubusercontent.com/94680549/236500390-3205477b-00f0-43f4-a22c-b24547da6eb5.jpg)

> For Further Settings Documention Visit: [Documentation]

[Documentation]: https://aka.ms/winget-settings



