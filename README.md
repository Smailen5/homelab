# homelab - Documentazione infrastruttura

## Indice

- [docs](docs/) - documentazione trasversale
  - [mappa-lan.md](docs/mappa-lan.md) - convenzione indirizzi LAN
  - [naming-lore.md](docs/naming-lore.md) - origine dei nomi
- [monday](monday/) - nodo Proxmox principale
  - [gateway](monday/gateway/README.md) - reverse proxy / tunnel
  - [portfolio](monday/portfolio/README.md) - server API
  - [mondayclaw](monday/mondayclaw/README.md) - agente AI
  - [qbittorrent](monday/qbittorrent/README.md) - client torrent
  - [wordpress](monday/wordpress/README.md) - blog di test
  - [template](monday/template/README.md) - template CT/LXC
- [router](router/README.md) - router/gateway LAN
- [yesterday](yesterday/pbs/README.md) - PBS e backup

## Struttura

Ogni macchina (nodo, VM o LXC) ha:

- `README.md` - descrizione pubblica: ruolo, servizi, sicurezza, note
- `CHANGELOG.md` - storico delle modifiche fatte sulla macchina

I dettagli di accesso (IP, utenti, porte, comandi) non sono pubblici: restano nei file `ACCESS.md` della repo privata.

## Principi

- **Nessun dato sensibile**: non troverai qui IP, hostname interni, utenti, credenziali o segreti dell'infrastruttura.
- **Segreti fuori dalla repo**: password, token e chiavi private sono gestiti in modo sicuro al di fuori di questo repository.
- **Documentazione descrittiva**: i file descrivono ruoli, servizi e scelte di design. La manutenzione vera e propria avviene sulle macchine.

## Nota sulla documentazione

Questo repository descrive l'infrastruttura homelab a scopo dimostrativo. Versioni, configurazioni e stato riflettono il momento dell'ultimo aggiornamento e potrebbero non essere allineati in tempo reale. I dettagli di accesso e configurazione sensibile non vengono pubblicati.
