# workstation

## Ruolo

PC di sviluppo usato per amministrare l'homelab: editor, terminale e client SSH verso le altre macchine.

## Servizi

- **Ambiente di sviluppo** - VS Code + WSL (Ubuntu 24.04):
  - accesso SSH alle macchine del homelab (nodo Proxmox, PBS, VM)
  - strumenti da terminale (git, container runtime)

## Sicurezza

- Nessun servizio in ascolto esposto: la macchina è solo client
- Accesso alle altre macchine esclusivamente via SSH con chiave
- Nessun DNS pubblico, nessun tunnel

## Note

- PC fisico, non gestito da Proxmox
- Indirizzo IP riservato via DHCP sul router

## Manutenzione

Vedi [CHANGELOG.md](CHANGELOG.md) per la storia della macchina.
