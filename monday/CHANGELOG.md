# Changelog - monday

## 2026-09-29

- Aggiornamento sistema: `pve-manager` 9.2.21, `qemu-server` 9.2.10, `pve-docs` 9.2.13, `libpve-storage-perl` 9.1.11 e `rsync` (aggiornamento di sicurezza)
- Installato `nvme-cli` come strumento di diagnostica NVMe, durante l'analisi del warning `smartd` sul disco di sistema → [caso 0001](../docs/casi/0001-warning-smartd-selftest-log-nvme.md)
- Verifica post-manutenzione: `systemctl --failed` pulito, VM/CT funzionanti e servizi esposti raggiungibili

## 2026-09-22

- Aggiornamento Proxmox: 88 pacchetti (`pve-manager` 9.2.20, `qemu-server` 9.2.8, `pve-firewall` 6.0.6, suite Ceph 19.2.6-pve4) e kernel `7.0.14-19`
- Rimozione vecchio kernel `7.0.14-14` (~1GB liberato)
- Pulizia sistema (`apt autoremove --purge` e `apt clean`)
- Riavvio del nodo; le VM/CT con avvio automatico sono ripartite
- Verifica post-manutenzione: kernel `7.0.14-19` attivo, VM/CT funzionanti e servizi esposti raggiungibili
- I kernel `6.17.x` restano installati come fallback di stabilità sulla serie `7.x`

## 2026-09-08

- Aggiornamento Proxmox: kernel 7.0.14-15, `pve-container` e firmware EDK2
- Rimozione vecchio kernel 7.0.14-12 (~1GB liberato)
- Pulizia sistema (`apt clean` e `apt autoremove`)
- Riavvio del nodo con downtime di circa 1 minuto
- Verifica post-manutenzione: VM/CT funzionanti e servizi esposti raggiungibili

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
