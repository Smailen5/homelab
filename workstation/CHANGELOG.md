# Changelog - workstation

## 2026-09-22

- Aggiornamento sistema: 22 pacchetti, con la toolchain Docker a `docker-ce` 29.8.1, `containerd.io` 2.3.5 e `docker-buildx-plugin` 0.37.1
- Nessun kernel coinvolto e nessun riavvio
- Ripristinato l'accesso SSH verso wordpress: su quella macchina mancava la chiave pubblica autorizzata
- Pulizia sistema (`apt autoremove --purge` e `apt clean`): nessun pacchetto da rimuovere
- Verifica post-manutenzione: `systemctl --failed` pulito

## 2026-09-08

- Aggiornamento sistema e toolchain Docker (CE, compose, buildx, containerd)

## 2026-09-01

- Aggiornamento sistema e pulizia
