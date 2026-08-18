# gateway

## Ruolo
Reverse proxy e tunnel: instrada il traffico verso le VM/CT interne e pubblica i servizi all'esterno.

## Servizi
- Nginx Proxy Manager (container `npm-app-1`)
- Cloudflare Tunnel (container `npm-tunnel-1`, progetto `~/npm`)

## Note
- ⚠️ Tutti i DNS locali puntano qui: NON spostare senza aggiornare DNS Cloudflare → rotte tunnel → upstream NPM → ufw → riserve FritzBox.
- Espone servizi interni tramite DNS locali e servizi pubblici tramite Cloudflare Tunnel.

## Stato
Ultima verifica: 2026-08-05