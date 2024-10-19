# STAN NA WERSJE: DEBIAN/GNU BOOKWORM 12 XFCE

## WAŻNE PLIKI
* fstab
```sh
/etc/fstab
```
* sources list
```sh
/etc/apt/sources.list
```
* grub
```sh
/etc/default/grub
```

## 1. AKTUALIZACJA I DEZAKTUALIZACJA
```sh
sudo apt update && sudo apt upgrade -y && sudo apt dist-upgrade -y && sudo apt autoremove -y && sudo apt install -y lsb-release
```
	
## 2. FIRMWARE LINUX
```sh
sudo apt install firmware-linux firmware-linux-nonfree firmware-misc-nonfree
```
	
## 3. INNY FIRMWARE
```sh
sudo apt install firmware-realtek firmware-atheros
```
	
## 4. STEROWNIKI KARTY GRAFICZNEJ
* NVIDIA

```sh
sudo apt install nvidia-detect
```

```sh
sudo nvidia-detect
```

```sh
sudo apt install nvidia-driver nvidia-settings
```

  * AMD

```sh
sudo apt install libdrm-amdgpu1 xserver-xorg-video-amdgpu
```

```sh
sudo apt install mesa-vulkan-drivers libvulkan1 vulkan-tools vulkan-validationlayers
```
		
## 5. FIRMWARE BROADCOM
```sh
sudo apt install broadcom-sta-dkms broadcom-sta-common firmware-brcm80211 firmware-iwlwifi
```
	
## 6. BLUETOOTH
```sh
sudo apt install bluetooth bluez bluez-firmware bluez-cups bluez-tools firmware-iwlwifi blueman
```

```sh
sudo systemctl enable bluetooth
```

```sh
sudo systemctl start bluetooth
```

```sh
sudo vim /etc/bluetooth/main.conf
```
	
## 7. MIKROKOD DO PROCESORÓW (SYSTEM AUTOMATYCZNIE INSTALUJE PODCZAS STANDARODWEJ INSTALACJI)
* INTEL

```sh
sudo apt install intel-microcode
```

* AMD

```sh
sudo apt install amd64-microcode
```
		
## 8. AUTOMATYCZNE WYSZUKIWANIE FIRMWARE
```sh
sudo apt install isenkram-cli
```

```sh
sudo isenkram-autoinstall-firmware
```

## 9. 32-BIT WINE
```sh
sudo dpkg --add-architecture i386
```
	
## 10. KODEKI
```sh
ffmpeg
```

```sh
rar unrar
```

```sh
libavcodec-extra
```

```sh
ttf-mscorefonts-installer
```
	
## 11. GRUB

```sh
sudo nano /etc/default/grub
```

 Czas uruchomienia 1 sekunda. Przy zmiennej quiet dać ```splash```.

 ```sh
 sudo update grub
```
	
## 12. LAPTOPY - ZARZĄDZANIE ENERGIĄ
```sh
sudo apt install tlp tlp-rdw
```

```sh
sudo tlp start
```

```sh
sudo tlp start
```
	
## 13. USTAWIENIA I PODSTAWOWE NARZĘDZIA
* gufw - zapora sieciowa
* mpv - odtwarzacz mulitmedialny
* audacious - odtwarzacz muzyki
* geany - odpowiednik Notepad++
* kolourpaint - odpowiednik Paint
* geepie - przeglądarka plików graficznych
* mc - terminalowy eksplorator plików
* git - narzędzie do klonowania repozytoriów GIT
* mugshot i menulibre - narzędzia do Whiskermenu
* inix - terminalowe narzędzie do odczytywania podzespołów komputera
* cmatrix - matrix
* fonts-noto-color-emoji - jak nie działają czcionki w Discord
* redshift-gtk - ochrona wzroku
* wireless-tools i net-tools - narzędzia do obłusgi sieci (terminal)
* lightdm-gtk-greeter-settings - ustawienia LighDM GTK GREETER
* htop - terminalowy menedżer zadań
* bpytop - extra terminalowy menedżer zadań
* bat - jakiś tam zamiennik git, może się przydać
* cifs-utils gvfs-backends  - dodatki sieciowe do Thunar

## 14. DRUKARKA HP STEROWNIKI
 * hplip
 * hplip-gui
	
## 15. WTYCZKI XFCE4 (SĄ ZAWARTE W PAKIECIE ```xfce4-goodies```)
* xfce4-cpufreq-plugin
* xfce4-cpugraph-plugin
* xfce4-sensors-plugin
* xfce4-systemload-plugin
* xfce4-battery-plugin
* xfce4-power-plugin
* thunar-archive-plugin
	
## 16. WYGLĄD
* papirus-icon-theme
* orchis-gtk-theme
	
## 17. FLATPAK
```sh
sudo apt install flatpak
```

```sh
sudo flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```
Jeśli masz środowisko GNOME to:
```sh
sudo apt install gnome-software-plugin-flatpak
```
	
## 18. ARDUINO BRAK ZEZWOLENIA NA PORT
```sh
sudo usermod -a -G dialout username
```
	
## 19. LIBREOFFICE INSTALACJA CAŁEGO PAKIETU
```sh
sudo apt install libreoffice lsb-release libreoffice-style* libreoffice-gtk3 libreoffice-l10n-pl libreoffice-help-pl hunspell-pl myspell-pl
```
	
## 20. USUWANIE PROGRAMÓW
```sh
sudo apt remove libreoffice-*
```

```sh
sudo apt remove exfalso quodlibet
```
	
## 21. KOMENDY APT USUWANIE
* usuwanie danego pakietu
```sh
sudo apt remove package
```
* usuwanie nieużywanych pakietów
```sh
sudo apt autoremove
``` 
* czyszczenie po instalacji
```sh
sudo apt autoclean
```
	
## 22. DODANIE REPOZYTORIUM NON-FREE I CONTRIB
```sh
sudo apt install software-properties-common -y
```

```sh
sudo apt-add-repository contrib non-free
```

**LUB**
		
```sh
sudo vim /etc/apt/sources.list
```

**CONTRIB** i **NON-FREE** do każdego

## 23. ŚRODOWISKO GRAFICZNE XFCE4
```sh
sudo apt install xfce4 lightdm
```

## 24. REDSHIFT CONFIG FILE
```sh
[redshift]
temp-day=5000
temp-night=4000
;gamma=0.8:0.7:0.8
gamma=1.000:1.000:1.000
location-provider=manual
adjustment-method=vidmode
;brightness=1.0:0.5

[manual]
lat=44.9
lon=-0.70
```

## 25. WINE
https://wine.htmlvalidator.com/install-wine-on-debian-12.html

## 26. SPOTIFY
https://www.spotify.com/pl/download/linux/

## 27. INNE OPROGRAMOWANIE
* gnumeric
* claws-mail
* pidgin
* catfish
* asunder
