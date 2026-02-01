# Installing and Configuring Linux(Ubuntu)

## <mark style="color:$primary;">Installing Ubuntu</mark>

1. Download [**Ubuntu**](https://ubuntu.com/download/desktop)
2. Install
3. after installing ubuntu on VM

```bash
sudo apt update && sudo apt upgrade -y
```

```bash
sudo apt install bzip2 tar gcc make perl git curl net-tools
```

```bash
sudo apt install linux-headers-generic
```

```bash
sudo apt install linux-headers-$(uname -r)
```

```bash
sudo apt autoremove && sudo apt autoclean
```

1. Install **`Guest Additions image`**
2. open terminal

```bash
cd /media && ls
```

```bash
cd location of VBOX_GAs_.. dir 
```

```bash
sudo ./VBoxLinuxAdditions.run
```

1. Restart Ubuntu VM now
   1. After installing ubuntu and guest addition images (take a snapshot)
   2. Clipboard & Drag & Drop → Bi-Directional

## <mark style="color:$primary;">Configuring Ubuntu</mark>

1. open terminal

```bash
cd ~/Documents && git clone <https://github.com/MalwareCube/SOC101_Free.git>
```

1. Extract each folder

```bash
cd ~/Documents/SOC101_Free/course_files
```

```bash
for f in *.zip; do unzip "$f" -d "${f%.zip}"; done && mv 0* ~/Desktop
```

```bash
mkdir -p ~/Desktop/soc101 && for f in *.zip; do d="${f%.zip}"; unzip "$f" -d "$d" && mv "$d" ~/Desktop/soc101/; done
```

1. Set taskbar to bottom
   1. Right click on Desktop → Desktop icon settings → (Dock) position on screen - bottom

```bash
cd ~/Documents/SOC101_Free/resources/install && chmod +x install.sh && ls
```

```powershell
./install.sh
```
