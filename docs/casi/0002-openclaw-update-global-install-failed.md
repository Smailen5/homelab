# Caso 0002: aggiornamento OpenClaw fallito (`global-install-failed`)

- Data: 2026-09-29
- Macchina: `mondayclaw`
- Dominio: troubleshooting di servizio · aggiornamento pacchetto

## Sintomo

`openclaw update` non porta a termine l'aggiornamento da 2026.9.4 a 2026.9.6.

```txt
OpenClaw update failed: global-install-failed.
Phases: requested -> staging -> validating (361.2s)
Failed: global install swap — Exit code: 1
```

Una verifica anormalmente lunga e lo scambio del pacchetto che esce con errore.

## Diagnosi

L'installazione non c'entra: node e npm aggiornati, registry ufficiale, albero globale integro, prefix corretto.

E' un difetto dell'updater installato (2026.9.4): su host occupati o dischi lenti il fingerprint del pacchetto scade dopo 30 secondi e viene letto come "albero modificato", quindi lo scambio fallisce. I 361 secondi della fase `validating` sono la firma del problema su questa VM. Ripetere l'aggiornamento con lo stesso updater riproduce l'errore, perche' i fix vivono nei pacchetti successivi al 2026.9.4 e un pacchetto nuovo non ripara un updater vecchio.

`--dry-run` non aiuta a capirlo: elenca le azioni ma non esegue lo scambio, quindi non tocca il passo che fallisce.

## Rimedio

Installazione manuale del pacchetto, che bypassa l'updater difettoso e lo sostituisce. Prima e' stato creato uno snapshot della VM con la RAM.

```bash
openclaw gateway stop
npm install -g openclaw@latest --allow-scripts=openclaw
openclaw doctor --fix
openclaw gateway restart
openclaw gateway status --deep
```

Note:

- senza `sudo`, altrimenti il pacchetto finisce fuori dal prefix dell'utente
- `--allow-scripts=openclaw` serve su npm oltre la 11.15
- il gateway gira come unit systemd utente, quindi serve `systemctl --user`
- la procedura si fa una volta sola, adesso l'updater installato e' quello nuovo

Il doctor ha migrato lo schema del database agente da v19 a v23, allineato i plugin ufficiali e riparato le sessioni. Da qui il rollback automatico non e' piu' possibile: lo snapshot e' la via di ripristino.

## Verifica

- CLI e gateway a 2026.9.6, runtime `running`, `Connectivity probe: ok`
- `npm ls -g --depth=0` mostra `openclaw@2026.9.6`
- la conferma finale si avra' al prossimo aggiornamento, quando `openclaw update` dovra' funzionare da solo
