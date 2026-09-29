# Changelog - mondayclaw

## 2026-09-29

- Aggiornamento sistema: kernel `6.12.111-1`
- Rimozione vecchio kernel `6.12.101` (~111 MB liberati)
- Gateway OpenClaw aggiornato da `2026.9.4` a `2026.9.6` con installazione manuale del pacchetto, per bypassare l'updater difettoso → [caso 0002](../../docs/casi/0002-openclaw-update-global-install-failed.md)
- Rettifica del 22/09: la causa del fallimento non era npm 11.19.0 ma un difetto dell'updater installato
- Riavvio programmato per il 2026-09-30 alle 03:00, per applicare il nuovo kernel
- Verifica post-manutenzione: `systemctl --failed` pulito e servizi raggiungibili

## 2026-09-22

- Aggiornamento sistema: 48 pacchetti, incluso Node.js 24.21.0
- Pulizia sistema (`apt autoremove --purge` e `apt clean`): nessun pacchetto da rimuovere
- Tentativo di aggiornamento del gateway OpenClaw da `2026.9.4` a `2026.9.5` non riuscito (errore di integrità del pacchetto npm, probabile incompatibilità con npm 11.19.0): rimandato alla prossima major, senza downgrade
- Verifica post-manutenzione: `systemctl --failed` pulito, gateway attivo e funzionante su `2026.9.4`

## 2026-09-15

- Seguito della manutenzione del 14/09: risolti gli effetti collaterali dell'aggiornamento del gateway
- Nella notte tra il 14 e il 15 (ore 00:40) aggiunte le chiavi OpenRouter e configurata una catena di fallback multi-provider, in sostituzione del fallback Gemini (costo inferiore, evita il blocco totale quando il provider principale è in tilt)
- Plugin allineati alla nuova versione, trigger dei cron aggiornati e heartbeat reso inerte
- Embedding riportati al server locale gestito (modello dedicato)
- Contesto dell'agente snellito (da ~30.000 a ~10.000 caratteri), dettagli spostati nei documenti del workspace
- Verifica: nessun servizio in errore, gateway attivo con configurazione valida

## 2026-09-14

- Downtime serale (22:02–22:15) causato dai timeout dei server DeepSeek: configurazione corretta, il gateway passava regolarmente al provider di fallback
- Aggiornamento gateway OpenClaw da `v2026.7.1-2` a `v2026.9.4` via CLI (la GUI non completava l'aggiornamento)
- Riavvio della macchina per allineare database e gateway

## 2026-09-08

- Verifica aggiornamenti: sistema già allineato, nessun aggiornamento necessario
- Pulizia sistema (`apt clean` e `apt autoremove`)
- Riavvio del nodo monday con downtime di circa 1 minuto

## 2026-09-01

- Aggiornamento sistema, kernel 6.12.107-1 e Node.js 24.20.0
- Rimozione vecchio kernel 6.12.100
- Riavvio con downtime di circa 1 minuto

## 2026-08-30

- Downtime 15:31-15:56
- Aggiornamento kernel

## 2026-08-25

- Verifica aggiornamenti: sistema già allineato, nessun aggiornamento necessario e pulizia eseguita

## 2026-08-24

- Downtime 15:00–16:00 per cambio contatore elettrico

## 2026-08-18

- Aggiornamento sistema (17 pacchetti)
- Installato kernel 6.12.101 (attivo dopo reboot)

## 2026-08-05

- Aggiornamento macchina e pulizia sistema
