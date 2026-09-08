# Changelog - monday

## 2026-09-01

- Verifica aggiornamenti: sistema già allineato, nessun aggiornamento o pulizia necessario

## 2026-08-30

- Riavvio forzato, monday non era collegato alla rete
- Downtime 15:31–15:56 per collegarlo al ups
- Aggiornamento sistema e pulizia

## 2026-08-25

- Aggiornamento sistema Proxmox e kernel
- Pulizia sistema con rimozione vecchio kernel obsoleto (~1GB liberato)
- Riavvio post-manutenzione per applicare il nuovo kernel
- Configurato e testato accesso SSH verso PBS (`yesterday`) tramite chiave

## 2026-08-24

- Downtime 15:00–16:00 per cambio contatore elettrico (interessate tutte le VM/CT di monday)

## 2026-08-18

- Aggiornamento sistema (apt upgrade)
- Rimossi kernel obsoleti (7.0.14-6 e 7.0.6-2, +2GB liberati)
- Reboot e verifica post-riavvio (systemctl --failed = 0)
- Verifica SMART NVMe: disco sano (0 errori, 3% usura)

## 2026-08-05

- Aggiornamento macchina e pulizia sistema
