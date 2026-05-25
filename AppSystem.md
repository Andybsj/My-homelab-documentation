### Mini PC server set-up
##### Start working on it at Saturday 9th May 2026
---
### Spec
* CPU : Intel N150 
* RAM : 16 GB ddr4
* Storage : 1 TB NVME SSD
---
### OS
#### [Debian](https://www.debian.org/) no GUI, only terminal set up for this with SSH applications selected for remote control from powershell.
---
### Applications
* [Tailscale](https://tailscale.com/)
  * *Usage* : Used as a secure, zero-config VPN mesh to access the server's internal services remotely without exposing public ports. Mainly used for phone and laptop to connect to my service.
  * *Status* : Fully working now (Got a error with tailscale serve using 443 port causing Nginx to break at Sunday 23 May 2026)
* [Docker](https://github.com/docker)
  * *Usage* : Used to isolate all applications into lightweight containers.
  * *Status* : downed (Fully working no error)
* [Docker composer](https://github.com/docker/compose)
  * *Usage:* Used to define and manage multi-container applications in simple `YAML` configuration files, allowing the entire stack to be deployed or updated with a single command.
  * *Status* : Fully working no error       
---
### Docker-compose applications
* **[Jellyfin](https://github.com/jellyfin/jellyfin)** (Created at Sunday 17th May 2026)
  * *Usage* : A self-hosted open-source media server used to stream media across most devices easily.
  * *Status* : Fully working.
* **[Nginxproxymanager](https://github.com/NginxProxyManager/nginx-proxy-manager)** (Created at Saturday 9th May 2026)
  * *Usage* : Manages reverse proxying, allowing secure domain routing and automatic SSL certificate management for internal tools.
  * *Status* : Fully working
* **[Vaultwarden](https://github.com/dani-garcia/vaultwarden)** (Created at Saturday 16th May 2026)
  * *Usage* : A lightweight, self-hosted Bitwarden-compatible API server used to securely manage and isolate personal passwords locally. is used with Nginxproxymanager and tailscale MagicDNS to make https certificate for one of api to work. Worked with browser extension, computer and phone.
  * *Status* : Fully working
* **[homepage](https://github.com/gethomepage/homepage)** (Created at Sunday 10th May 2026)
  * *Usage* : Customizable decent looking application dashboard that serves as a single entry point to monitor service status and shortcuts.
  * *Status* : Partially working at time of writing this (Sunday 24th May 2026))
* **[uptimekuma](https://github.com/louislam/uptime-kuma)** (25th May 2026)
  * *Usage* : A self-hosted monitoring tool to track service availability and send alerts if any container or network device goes offline, mostly used to check if website is having a problem in backend. (will move to a NAS when i get one)
  * *Status* : Fully working 
* **[homarr](https://github.com/homarr-labs/homarr)** (Created at Saturday 9th May 2026)
  * *Usage* : Used to checked docker status and have cool dashboard. Also serves as a single entry point to monitor service status and shortcuts.
  * *Status* : Removed due to high ram usage and CPU spike Replaced with homepage
---
### Maintenance & History
To keep this document clean, the full history of updates, configuration changes, and installation dates for this machine is tracked separately.
#### Started from Sunday 26th May 2026
[View the full Server A Change Log](AppSystem-changelog.md)

