# multi-nm-vpn

Parses output from `nmcli` to show the current connected VPN name/status. Captures multiple vpn connections

# Requirements

  - NetworkManager/`nmcli`
  - `bash`

# Usage

`multi-nm-vpn` gets connections info from `nmcli`. 
`monitor` variable can be set to monitor the specific connection.

## Output

For every vpn connection
  - `VPN: "Name":"ON|OFF"`

If `monitor` is not set, the output is coloured yellow ("\#FFAE00").
If `monitor` is set, the output is coloured purple ("\#e180fc"), when connected to the monitored vpn, and red ("\#FF0000"), when not connected.

# Config

``` ini
[multi-nm-vpn]
label=VPN 
monitor=PVPN
interval=10
separator=false
```
