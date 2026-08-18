# monday

Nodo Proxmox principale dell'homelab.

## Hardware

- Modello: GMKtec G10
- CPU: Ryzen 5
- RAM: 16GB DDR4
- Storage: 
  - NVMe ~459GB interno (sistema + dischi VM)
  - SATA ~480GB esterno (storage dati aggiuntivo)

## Ruolo

- Hypervisor Proxmox VE
- Host di VM e LXC per servizi interni ed esposti
- Backup orari su PBS (`yesterday`)

## VM / LXC ospitati

- [gateway](gateway/README.md) - reverse proxy e tunnel
- [portfolio](portfolio/README.md) - server API
- [mondayclaw](mondayclaw/README.md) - agente AI
- [qbittorrent](qbittorrent/README.md) - client torrent
- [wordpress](wordpress/README.md) - blog di test
- [template](template/README.md) - template CT/LXC

## Note

- Piano upgrade RAM quando i prezzi calano
- Backup orari su PBS

## Stato

Ultima verifica: 2026-08-04