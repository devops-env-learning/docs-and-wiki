## Usunięcie komunikatu o braku licencji podczas logowania do panelu Proxmox
- Zalogować się na root z poziomu terminala lub z poziomu panelu Proxmox (tam wejść w pve- > Shell)
    ```bash
    cp /usr/share/javascript/proxmox-widget-toolkit/proxmoxlib.js /usr/share/javascript/proxmox-widget-toolkit/proxmoxlib.js.bak && sed -i '/checked_command: function (orig_cmd) {$/a\    return (typeof orig_cmd === "function" && (orig_cmd(), true));' /usr/share/javascript/proxmox-widget-toolkit/proxmoxlib.js && systemctl restart pveproxy.service
    ```