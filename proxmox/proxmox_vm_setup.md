# Wymagania
- Zainstalowane VMWare Workstation PRO
## Tworzenie VM Proxmox w VMWare Workstation PRO
- Create a New Virtual Machine
- Custom (advanced)
- Workstation 25H2 or later
- Install disc image file (iso) - pobrać najnowsze z http://proxmox.com/en/downloads/proxmox-virtual-environment/iso
- Linux -> wybrać wersję Debiana, na której bazuje Proxmox, np Proxmox 9.1 bazuje na Debian 13.2
- Nadać nazwę, np. Proxmox
- Procesor, np. 1 cpu, 8 rdzeni
- Pamięć, np. 24gb = 24576 MB
- NAT network
- LSI Logic (Recommanded)
- SCSI (Recommended)
- Create a new virtual disk
- Maximum disk size (GB) - na start z 300GB + zaznaczyć opcję `Store virtual disk as a single file`
- Zapisać dysk wirtualny (.vmdk) na w miare możliwosci szybkim dysku
- Uruchomić VM
## Instalacja Proxmox
Po uruchomieniu VM powinen odpalić sie instalator Proxmox
- Install Proxmox VE (Graphical)
- I agree (akceptacja licencji)
- Wybrać dysk, powinen być tylko jeden do wyboru (300gb)
- Country: Poland
- Podać hasło do Proxmoxa i adres e-mail
- nadać nazwę proxmoxa, np. pve.vmproxmox
- zaakceptować wybory i rozpocząć instalację
- po zakończeniu instalacji Proxmox, maszyna sie zrestartuje i Proxmox uruchomi się sam
- po uruchomieniu Proxmoxa z poziomu terminala można zalogować się za pomocą użytkownika root i hasła ustawionego podczas instalacji
- Jeżeli podczas instalacji ustawiłeś sięć `NAT` to z poziomu hosta, czyli np. Windowsa możesz zalogować się do panelu Proxmoxa w przeglądarce, w oknie terminala w Proxmoxie jest napisany adres np: https://192.168.80.128:8006
