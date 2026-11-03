# Red-Empresarial-Linux-VPN-DNS-DHCP
Infraestructura Linux de 2 redes (14 VMs) unidas por OpenVPN: DNS primario/secundario, DHCP Failover, Web, FTP y correo entre dominios.

Proyecto individual del CDT Telemática, módulo Servidores Linux (INA).

Dos organizaciones independientes, RED-A (telematica.edu) y RED-B (mep.edu),
con 14 máquinas virtuales en VirtualBox, conectadas por una VPN.

## Redes

| | RED-A | RED-B |
|---|---|---|
| Dominio | telematica.edu | mep.edu |
| LAN | 192.168.10.0/24 | 192.168.50.0/24 |
| Túnel VPN | 10.0.0.1 | 10.0.0.2 |

## Servicios (en cada red)

- DHCP con failover entre dos servidores
- DNS primario y secundario con transferencia de zona (Bind9)
- Servidor Web con página propia
- Servidor FTP con usuarios locales
- Servidor de correo entre dominios (registros MX)
- Gateway con VPN OpenVPN entre las dos LAN

## Pruebas realizadas (15)

DHCP en ambas redes, DNS local y remoto, VPN, ping entre LAN,
Web y FTP locales y remotos, correo local y entre dominios,
DNS Failover y DHCP Failover.

## Documentación

Informe completo con configuraciones y capturas en [`Documentacion/`](Documentacion/).

## Tecnologías
Debian, Bind9, ISC-DHCP, OpenVPN, FTP, VirtualBox
