I largely followed the instructions at https://community.openvpn.net/openvpn/wiki/HOWTO . The following applies to OpenVPN deployment on Windows 10.

## Setup routing services on the OpenVPN server
Open Windows Services on the OpenVPN server, enable Routing and Remote Access service. Choose "Startup type: Autotamatic (Delayed Start)" and "Subsequent failures: Restart the Service"

## Setup port forwarding on the router

    Protocol TCP and UDP
    WAN host start/end empty
    WAN start/end port 1194
    LAN host 192.168.20.89
    LAN start/end port 1194

## Setup static routing on the router

    address 10.8.0.0
    mask 255.255.255.0
    gateway 192.168.20.89
