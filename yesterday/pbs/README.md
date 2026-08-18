# pbs (yesterday)

## Ruolo
Proxmox Backup Server: custodisce i backup orari delle VM di **monday**.

## Servizi
- **PBS** - Proxmox Backup Server (backup e restore)

## Sicurezza
- Esposto esclusivamente in rete locale
- SSH blindato: niente root, niente password, solo chiavi

## Note
- PC fisico dedicato: Intel Core i3-6098P, 8GB RAM
- Dischi: 500GB (backup) + 1TB (disco aggiuntivo)

## Manutenzione
[Changelog](CHANGELOG.md)