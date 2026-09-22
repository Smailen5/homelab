# Changelog — wordpress

## 2026-09-22

- Aggiornamento sistema: `tzdata` 2026c
- Ripristinato l'accesso SSH dalla workstation: sulla macchina mancava la chiave pubblica autorizzata
- Pulizia sistema (`apt autoremove` e `apt clean`): nessun pacchetto da rimuovere
- Verifica post-manutenzione: `systemctl --failed` pulito

## 2026-09-08

- Verifica aggiornamenti: sistema già allineato, nessun aggiornamento necessario
- Pulizia sistema (`apt clean` e `apt autoremove`)
- Riavvio del nodo monday con downtime di circa 1 minuto

## 2026-09-01

- Verifica aggiornamenti: sistema già allineato, nessun aggiornamento o pulizia necessario

## 2026-08-25

- Verifica aggiornamenti: sistema già allineato, nessun aggiornamento necessario e pulizia eseguita

## 2026-08-24

- Downtime 15:00–16:00 per cambio contatore elettrico

## 2026-08-18

- Sistema già allineato, nessun aggiornamento necessario
- Disattivato `systemd-networkd-wait-online` (timeout benigni a ogni boot)

## 2026-08-05

- Aggiornamento pacchetti e pulizia sistema
