# Changelog - portfolio

## 2026-09-29

- Aggiornamento sistema: `containerd.io` 2.3.6 e kernel `6.12.111-1`
- Rimozione vecchio kernel `6.12.101` (~111 MB liberati)
- Riavvio programmato per il 2026-09-30 alle 03:00, per non togliere il sito durante il giorno
- Verifica post-manutenzione: `systemctl --failed` pulito e servizi esposti raggiungibili

## 2026-09-22

- Aggiornamento sistema: 44 pacchetti (base di sistema, Perl/Python, BIND9, curl, toolchain Docker)
- Aggiornamento immagini Docker (`docker compose pull` e `up -d`) e pulizia (`docker image prune -f`, 1,18 GB recuperati)
- Pulizia sistema (`apt autoremove --purge` e `apt clean`): nessun pacchetto da rimuovere
- Verifica post-manutenzione: `systemctl --failed` pulito e servizi esposti raggiungibili

## 2026-09-08

- Aggiornamento piattaforma Docker (CE, containerd, compose, buildx)
- Aggiornamento immagini Docker (`docker compose pull` e `up -d`)
- Pulizia immagini Docker (`docker image prune -f`)
- Pulizia sistema (`apt clean` e `apt autoremove`)
- Riavvio del nodo monday con downtime di circa 1 minuto

## 2026-09-01

- Aggiornamento sistema e kernel 6.12.107-1
- Rimozione vecchio kernel 6.12.100
- Riavvio con downtime di circa 1 minuto
- Immagini Docker già aggiornate e pulite

## 2026-08-30

- Downtime 15:31–15:56
- Aggiornamento kernel
- Aggiornamento immagini Docker e pulizia

## 2026-08-25

- Verifica aggiornamenti: sistema già allineato, nessun aggiornamento necessario e pulizia eseguita

## 2026-08-24

- Downtime 15:00–16:00 per cambio contatore elettrico

## 2026-08-18

- Aggiornamento sistema
- Aggiornamento immagini Docker
- Pulizia immagini Docker

## 2026-08-05

- Aggiornamento macchina e pulizia sistema
