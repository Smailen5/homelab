# ups

## Ruolo

Gruppo di continuità (UPS) che alimenta le macchine critiche della rete durante blackout e sbalzi di tensione.

## Servizi

- **Backup elettrico** - alimentazione di emergenza per:
  - nodo Proxmox (`monday`)
  - PBS (`yesterday`)
  - router FritzBox
- **Protezione** - filtro contro sbalzi di tensione

## Sicurezza

- Nessun accesso di rete: dispositivo puramente elettrico
- Nessun DNS, tunnel o porta esposta

## Note

- Dispositivo fisico, non VM/CT
- Prese limitate: estese con due ciabatte custom da 4 slot realizzate in casa
- Antenna Eolo non ancora collegata (cavo troppo corto, serve prolunga)

## Manutenzione

Vedi [CHANGELOG.md](CHANGELOG.md) per la storia del dispositivo.
