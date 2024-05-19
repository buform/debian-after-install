# STAN NA WERSJE: DEBIAN/GNU BOOKWORM 12 XFCE

## WAŻNE PLIKI
* fstab

```/etc/fstab```
* sources list

```/etc/apt/sources.list```
* grub

```/etc/default/grub```

## 1. AKTUALIZACJA I DEZAKTUALIZACJA
```sudo apt update && sudo apt upgrade -y && sudo apt dist-upgrade -y && udo apt autoremove -y && sudo apt install -y lsb-release```
	
## 2. FIRMWARE LINUX
```sudo apt install firmware-linux firmware-linux-nonfree firmware-misc-nonfree```
	
## 3. INNY FIRMWARE
```sudo apt install firmware-realtek firmware-atheros```
	
## 4. STEROWNIKI KARTY GRAFICZNEJ
* NVIDIA

```sudo apt install nvidia-detect```

```sudo nvidia-detect```

```sudo apt install nvidia-driver nvidia-settings```

  * AMD

```sudo apt install libdrm-amdgpu1 xserver-xorg-video-amdgpu```

```sudo apt install mesa-vulkan-drivers libvulkan1 vulkan-tools vulkan-validationlayers```
		
## 5. FIRMWARE BROADCOM
```sudo apt install broadcom-sta-dkms broadcom-sta-common firmware-brcm80211 firmware-iwlwifi```
	
## 6. BLUETOOTH
```sudo apt install bluetooth bluez bluez-firmware bluez-cups bluez-tools firmware-iwlwifi blueman```

```sudo systemctl enable bluetooth```

```sudo systemctl start bluetooth```

```sudo vim /etc/bluetooth/main.conf```
	
## 7. MIKROKOD DO PROCESORÓW
* INTEL

```sudo apt install intel-microcode```

* AMD

```sudo apt install amd64-microcode```
		
## 8. AUTOMAYCZNE WYSZUKIWANIE FIRMWARE
```sudo apt install isenkram-cli```

```sudo isenkram-autoinstall-firmware```

## 9. 32 BIT WINE
```sudo dpkg --add-architecture i386```
	
## 10. KODEKI
```sudo apt install ffmpeg ttf-mscorefonts-installer rar unrar libavcodec-extra```
	
## 11. GRUB

```sudo nano /etc/default/grub```

 Czas uruchomienia 1 sekunda. Przy zmiennej quiet dać ```splash```.
	
## 12. LAPTOPY - ZARZĄDZANIE ENERGIĄ
```sudo apt install tlp tlp-rdw```

```sudo tlp start```
	
## 13. DODATKOWE PACZKI I PROGRAMY
* inxi
* neofetch
* mc
* git
* bpytop
* bat
* lightdm-gtk-greeter-settings
* mugshot
* gufw
* menulibre
* cmatrix
* gvfs-backends
* cifs-utils
* fonts-noto-color-emoji
* thunar-archive-plugin
* redshift-gtk
* htop engrampa
* eom
* mpv
* audacious
* krita
* geany
* kolourpaint
* net-tools
* wireless-tools atril
* xfce4-goodies
	
## 14. DRUKARKA HP
 * hplip
 * hplip-gui
	
## 15. WTYCZKI XFCE4
* xfce4-cpufreq-plugin
* xfce4-cpugraph-plugin
* xfce4-sensors-plugin
* xfce4-systemload-plugin
* xfce4-battery-plugin
* xfce4-power-plugin
	
## 16. WYGLĄD
* papirus-icon-theme
* orchis-gtk-theme
	
# 17. FLATPAK
```sudo apt install flatpak```

```flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo```
	
## 18. ARDUINO BRAK ZEZWOLENIA NA PORT
```sudo usermod -a -G dialout username```
	
## 19. LIBREOFFICE
```sudo apt install libreoffice lsb-release libreoffice-style* libreoffice-gtk3 libreoffice-l10n-pl libreoffice-help-pl hunspell-pl myspell-pl```
	
## 20. USUWANIE PROGRAMÓW
```sudo apt remove libreoffice-*```

```sudo apt remove exfalso quodlibet```
	
## 21. KOMENDY APT USUWANIE
```sudo apt remove```

```sudo apt autoremove```

```sudo apt autoclean```
	
## 22. DODANIE REPOZYTORIUM NON-FREE I CONTRIB
```sudo apt install software-properties-common -y```

```apt-add-repository contrib non-free```
		
```sudo vim /etc/apt/sources.list```

CONTRIB i NON-FREE do każdego

## 23. ŚRODOWISKO GRAFICZNE XFCE4
```sudo apt install xfce4 lightdm```
