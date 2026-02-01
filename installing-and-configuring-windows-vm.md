# Installing & Configuring Windows VM

## Installing Windows Evaluation Center

* Install virtualbox
* Install [**windows**](https://info.microsoft.com/ww-landing-windows-11-enterprise.html?lcid=en-IN)
  * After installing windows and guest addition images (take a snapshot)
  * Clipboard & Drag & Drop → Bi-Directional

## Configuring Windows

* Turn off antivirus (windows defender)
* to show why turn off
  * execute **`Invoke mimikatz`** in powershell
  * visit [eicar](https://www.eicar.org/download-anti-malware-testfile/) → save .txt content

Enter below command in Powershell (Run powershell as administrator)

```powershell
Set-MpPreference -DisableRealtimeMonitoring $true
```

```powershell
Set-MpPreference -DisableScanningNetworkFiles $true
```

```powershell
Set-MpPreference -DisableBlockAtFirstSeen $true
```

```powershell
reg add "HKLM\\SOFTWARE\\Policies\\Microsoft\\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f
```

* Try running mimikatz again (should work)
* Install [**Git**](https://git-scm.com/install/windows) in windows VM (Next → Next → Install)
* open cmd → **`cd Documents`**
* enter below command :

```powershell
git clone <https://github.com/MalwareCube/SOC101_Free.git>
```

```powershell
cd Documents/SOC101_Free/course_files
```

* Create a folder called **`SOC Fundamentals`** and move every folder in it
* Create shortcut for **`Powershell`** & **`Command prompt`** on Desktop
