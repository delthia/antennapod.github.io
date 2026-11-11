Did you see that there's a new AntennaPod release and wonder:
* *why isn't the latest version not on F-Droid yet?*
* *when will the new release be available on F-Droid?*

If the new version is in beta, it is *only* available through Google Play ([here
is why]{1}). When we think it's ready we upload it to Google Play. A few days
later, when we're confident there are no critical bugs, we tag the release on
GitHub. F-Droid then has to find out about this release, build it and make it
available. All these steps may take some time. Due to the different steps and
because we are not involved in publishing releases on F-Droid, we can't tell
when exactly the latest version will be available there. It usually takes a few
days after the release is tagged on GitHub.

In short: it may take some time. Please be patient.

### The steps of getting a new version on F-Droid
1. After we create a [release](/documentation/general/beta#f-droid), F-Droid
   needs to detect that something in AntennaPod changed. For this, F-Droid runs
   an update checker server about every 2 days.
2. After F-Droid detects that there is a new AntennaPod release, it builds the
   app. With this, F-Droid makes sure that the app you download really matches
   the source code that AntennaPod publishes. Because there are many apps to
   build, the F-Droid server takes an additional 1-2 days to build the app.
3. Finally, the resulting app needs to get signed cryptographically. This
   happens on a computer that is not connected to the internet. A person at
   F-Droid needs to take the app and physically walk it to that special
   computer. How long this takes depends on how often the person walks to that
   special computer. Usually, this step takes an additional 1-2 days after the
   app was built.
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

### What you can do if it takes longer than expected
As you can see it can easily take a week before a new AntennaPod release is
available on F-Droid. If an update is still not available more than a week after
its release, feel free to let us know by creating a post on our [forum]{1}, and
we'll investigate it.

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
