# Changelog — pbs (yesterday)

## 2026-09-01

- Aggiornamento sistema, kernel Proxmox 7.0.14-14 e ZFS 2.4.4
- Rimozione vecchio kernel 7.0.14-8
- Riavvio con downtime di circa 1 minuto

## 2026-08-30

- Downtime 15:31-15:56
- Aggiornamento configurazione bios
- Sostituzione pila bios
- Sostituita connessione diretta al UPS

## 2026-08-25

- Aggiornamento pacchetti e pulizia sistema
- Aggiunta chiave pubblica SSH del nodo `monday` nelle chiavi autorizzate (abilitato accesso SSH diretto tra i nodi)

## 2026-08-18

- Aggiornamento sistema e kernel 7.0.14-12-pve (reboot)
- Pulizia sistema (apt clean + autoremove)
- Cablaggio: tentato cavo Ethernet CAT5e non CCA crimpato custom, velocità limitata a 100Mbit → ripristinato cavo cat6 esistente (5m); cavo custom da sostituire con cavo certificato
- BIOS: perdita configurazione dopo spegnimento prolungato (batteria CMOS da sostituire)
- Collegato all'UPS

## 2026-08-05

- Aggiornamento PBS 4.2.4 + kernel 7.0.14-8 (reboot fatto)
- Hardening SSH: root disabilitato, solo chiavi
- Backup orario automatico attivo su tutte le VM/LXC di monday
- Pulizia sistema
