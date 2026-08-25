# wordpress

## Ruolo

WordPress di test (TurnKey Linux) su **monday**. Serve per fare pratica con WordPress.

## Servizi

- **WordPress** - sito di test con stack LAMP:
  - Apache HTTP Server
  - MariaDB come database

## Sicurezza

- Esposto tramite Cloudflare tunnel, ma non pubblicizzato ( uso personale di test )
- Accesso admin protetto da credenziali
- Container unprivileged con firewall pve-firewall attivo sul nodo

## Note

- CT 102 · IP statico (riserva FritzBox come backup)
- Ambiente di test, non di produzione

## Manutenzione

[Changelog](CHANGELOG.md)
