# Connecting to eduroam

The first step to doing anything is, of course, to connect to the `eduroam` network.

Here's how to do that with your networking system:

## NetworkManager
*Read about [NetworkManager](https://wiki.archlinux.org/title/NetworkManager) on the Arch Linux Wiki*

### GUI (nm-connection-editor)

Using the NetworkManager GUI, simply detect the `eduroam` network and then configure it like this:

- **Authentication**: Protected EAP (PEAP)
- **No CA certificate is required**
- **Username**: (your NCSSM email)
- **Password**: (your NCSSM account password)

### Connection File

The following is a template `.nmconnection` file to place in `/etc/NetworkManager/system-connections/`.

You can get your interface device by running `nmcli device` and looking for the one labeled `wifi`.

```ini
[connection]
id=eduroam
uuid=08627a59-7595-456a-a7c8-6b9b21beeb3b # [or generate a UUID]
type=wifi
interface-name=[your interface ex. wlp170s0]

[wifi]
mode=infrastructure
ssid=eduroam

[wifi-security]
key-mgmt=wpa-eap

[802-1x]
eap=peap;
identity=[NCSSM email]
password=[NCSSM password]
phase2-auth=mschapv2

[ipv4]
method=auto

[ipv6]
addr-gen-mode=stable-privacy
method=auto
```

## Others?

If there's any other networking system you use please contribute a guide for it!
