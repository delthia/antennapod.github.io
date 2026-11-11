Med AntennaPod kan du spesifisere abonnementer (podkast-strømmer) som skal
oppdateres regelmessig (se [Oppdatering av
podcaster](/documentation/automation/refreshing-podcasts)).

Hvis du har mer komplekse behov, kan du bruke forskjellige tredjeparts
automatiseringsapplikasjoner med AntennaPod for å gjøre det. For eksempel:
- Få abonnementene oppdatert på starten av dagen: Slå på WiFi kl. 07.00, og
  oppdater deretter AntennaPod-strømmer.
- Få abonnementene dine før du kjører hjem: kl. 17.00 på hverdager oppdateres
  abonnementene.

## Generell instruks
I automatiseringsapplikasjonen din kan du få AntennaPod til å oppdatere
abonnementene sine ved å sende en 'kringkasting' (det kan vises som en type
Android-intensjon) med følgende innstillinger:
- Pakkenavn: `de.danoeh.antennapod`
- Klassenavn:
  `de.danoeh.antennapod.net.download.service.feed.FeedUpdateReceiver`

## Instruks for noen automasjonsprogrammer

### Automate ([nettsted](https://companion.home-assistant.io/docs/notifications/notification-commands/#broadcast-intent))
I en flyt skal du legge til en blokk av type `APPS` → `Broadcast send` og angi
```
action: notify.mobile_app_<SOME-ANDROID-MOBILE-DEVICE>
metadata: {}
data:
  message: command_broadcast_intent
  data:
    intent_package_name: de.danoeh.antennapod
    intent_class_name: de.danoeh.antennapod.net.download.service.feed.FeedUpdateReceiver
    intent_action: Something random - cannot be empty
```

### Tasker ([nettside](https://llamalab.com/automate/))
Opprett en oppgave. I oppgaven legger du til en handling
1. Velg `System`
2. Velg `Send Intensjon`

### Llama - Location Profiles ([nettside](https://tasker.joaoapps.com/))
Opprett en begivenhet (Llama-automasjonsregel). I hendelsen,
1. Legg til en type Android-intensjon.
2. Angi intensjonforsendelsesmetoden til `Kringkasting`.
3. Pakkenavn skal være `de.danoeh.antennapod`
4. Angi klassenavnet
   `de.danoeh.antennapod.net.download.service.feed.FeedUpdateReceiver`
5. Legg til andre betingelser/handlinger som det passer deg.
6. You can leave the other fields blank

---

Som en snarvei kan du klikke [denne lenken]{1} for å opprette en
eksempelhendelse å begynne med.
