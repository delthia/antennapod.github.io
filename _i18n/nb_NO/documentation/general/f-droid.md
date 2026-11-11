La du merke til at det er en ny utgivelse av AntennaPod og lurer på:
* *hvorfor er ikke siste versjonen på F-Droid ennå?*
* *når blir den nye utgivelsen tilgjengelig på F-Droid?*

Dersom den nye versjonen er i beta finnes den *bare* på Google Play ([les
hvorfor her]{1}). Når vi mener den er klar laster vi den opp til Google Play.
Noen dager senere, når vi er sikker på at det ikke er noen kritiske feil merker
vi utgivelsen på GitHub. F-Droid må deretter finne ut om denne utgivelsen, bygge
den og gjøre den tilgjengelig. Alle disse stegene tar litt tid. På grunn av de
ulike stegene og fordi vi ikke er involvert i utgivelsene på F-Droid, kan vi
ikke fortelle nøyaktig når den siste versjonen blir tilgjengelig der. Det tar
vanligvis noen dager etter utgivelsen er merket på GitHub.

Kort fortalt: det tar litt tid. Vær tålmodig.

### Stegene for å få en ny versjon på F-Droid
1. Etter at vi har opprettet en
   [utgivelse](/documentation/general/beta#f-droid), må F-Droid oppdage at noe i
   AntennaPod har endret seg. For dette kjører F-Droid en oppdateringskontroll
   omtrent annenhver dag.
2. Etter at F-Droid oppdager at det er en ny AntennaPod-utgivelse bygger de
   appen. Med dette sørger F-Droid for at appen du laster ned virkelig samsvarer
   med kildekoden som AntennaPod publiserer. Fordi det er mange apper å bygge
   bruker F-Droid-serveren ytterligere 1-2 dager å bygge appen.
3. Til slutt må den resulterende appen signeres kryptografisk. Dette skjer på en
   datamaskin som ikke er koblet til internett. En person hos F-Droid må ta med
   seg appen og fysisk gå med den til den spesielle datamaskinen. Hvor lang tid
   dette tar avhenger av hvor ofte personen går til den spesielle datamaskinen.
   Vanligvis tar dette trinnet ytterligere 1-2 dager etter at appen ble bygget.
4. F-Droid systems check the AntennaPod repository and detect a new release. The
   update checker server runs daily (overnight in Europe).
5. F-Droid systems build the app. They do this to make sure the app you download
   matches the source code that we publishe. Because there are many apps to
   build, the F-Droid server takes 1 to 2 days to build the app.
6. An F-Droid contributor signs the build cryptographically. To improve
   security, the contributor needs to take the app and physically walk it to a
   dedicated computer which is not connected to the internet. When all apps are
   signed, the contributor uploads them to the F-Droid systems. This usually
   takes 1 to 2 days.
7. F-Droid systems process the new apps, adding the new AntennaPod release in
   their index.

At this point we consider it 'released on F-Droid'. But remember that your
F-Droid client (the 'app store') also needs to refresh its local copy of the
index. Only after that you'll get prompted about the latest AntennaPod release.

### Hva du kan gjøre om det tar lenger en forventet
Som du ser kan det lett ta en ukes tid før en ny utgivelse av AntennaPod er
tilgjengelig på F-Droid. Om en oppdatering fremdeles ikke er tilgjengelig over 1
uke etter utgivelse kan du gi oss et vink ved å lage en post på [forumet
vårt]{1} så skal vi finne ut av det.

### What you can do if you're eagerly waiting
Did we not tag the [release on
GitHub](https://github.com/AntennaPod/AntennaPod/releases) yet? Then please just
wait. The update is in beta and not ready for public release.

We *did* tag the release on GitHub? As the F-Droid team
[notes](https://gitlab.com/fdroid/wiki/-/wikis/FAQ#how-long-does-it-take-for-my-app-to-show-up-on-website-and-client):
"don't panic before 7 days have passed, please."

* Did those 7 days pass since we tagged the release on GitHub? Feel free to let
  us know by creating a post on our [forum](https://forum.antennapod.org/).
  We'll take a look.
* Did we tag the release 7 days ago or less? Then please just wait. Or
  investigate where we are in the process.

#### Investigate current status
If you want, you can follow these steps to get an idea of the progress:
1. Check if and when the [release was tagged on
   GitHub](https://github.com/AntennaPod/AntennaPod/releases/latest) (you may
   need to hover, for example, 'last week' to see the exact date on GitHub). If
   so, it should soon be picked up by the update checker.
2. Check if [F-Droid's AntennaPod versions
   list](https://gitlab.com/fdroid/fdroiddata/-/commits/master/metadata/de.danoeh.antennapod.yml?author=checkupdates%20bot)
   was updated since then. If so, it should soon be processed by the build
   server.
3. Check if AntennaPod was built in the [running
   cycle](https://monitor.f-droid.org/builds/running) or the [last
   cycle](https://monitor.f-droid.org/builds/build). You can also use the app
   [F-Droid build
   status](https://f-droid.org/en/packages/de.storchp.fdroidbuildstatus/) for
   this. If so, it should soon be cryptographically signed by an F-Droid
   contributor.
    * Note that there's no queue for apps that need to be built. AntennaPod is
      not listed in the success and fail lists yet, and you want to know if it
      will be built?
        1. click on 'fdroiddata version' @ commit of a build cycle
        2. click on 'Browse files'
        3. click on 'Find file'
        3. copy and paste `de.danoeh.antennapod`
        4. open the file
        5. check if it includes the latest release
