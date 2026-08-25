# qbittorrent

## Ruolo

Client torrent (qBittorrent) in container LXC (CT 104) ospitato su **monday**, dedicato ai download gestiti in autonomia nella rete locale.

## Servizi

- **qBittorrent** - client torrent open-source con WebUI integrata:
  - gestione completa dei download da browser (aggiunta/rimozione torrent, priorita', limiti di velocita')

## Sicurezza

- Esposto esclusivamente in rete locale (nessun DNS pubblico, nessun tunnel)
- Accesso WebUI protetto da credenziali

## Note

- CT 104 · container LXC leggero sul nodo Proxmox
- Download su disco esterno al container via bind mount

## Manutenzione

Vedi [CHANGELOG.md](CHANGELOG.md) per la storia del dispositivo.
