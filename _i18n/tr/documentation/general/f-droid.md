Yeni bir AntennaPod sürümü olduğunu gördünüz mü ve şunu merak ettiniz mi:
* _why is the latest version not on F-Droid yet?_
* _when will the new release be available on F-Droid?_

Yeni sürüm beta aşamasındaysa, * sadece * Google Play üzerinden kullanılabilir
([nedeni şu]{1}). Hazır olduğunu düşündüğümüzde Google Play'e yükleriz . Birkaç
gün sonra, kritik bir hata olmadığından emin olduğumuzda, sürümü GitHub'da
etiketleriz. Daha sonra F-Droid'in bu sürümü bulması, derlemesi ve kullanıma
sunması gerekir. Tüm bu adımlar biraz zaman alabilir. Farklı adımlar nedeniyle
ve F-Droid'de sürüm yayınlamakla ilgilenmediğimiz için , en son sürümün tam
olarak ne zaman orada kullanılabilir olacağını söyleyemeyiz. Genellikle sürüm
GitHub'da etiketlendikten sonra birkaç gün sürer.

Kısaca: biraz zaman alabilir. Lütfen sabırlı olun.

### F-Droid'de yeni bir sürüm edinmenin adımları
1. Bir [sürüm](https://github.com/ AntennaPod / AntennaPod /releases)
   oluşturduktan sonra , F-Droid'in AntennaPod'da bir şeyin değiştiğini tespit
   etmesi gerekir . Bunun için F-Droid yaklaşık her 2 günde bir güncelleme
   denetleyici sunucusu çalıştırır.
2. F-Droid yeni bir AntennaPod sürümü olduğunu tespit ettikten sonra uygulamayı
   oluşturur. F-Droid bununla indirdiğiniz uygulamanın AntennaPod'un yayınladığı
   kaynak koduyla gerçekten eşleştiğinden emin olur. Oluşturulacak çok sayıda
   uygulama olduğu için F-Droid sunucusunun uygulamayı oluşturması 1-2 gün daha
   sürer.
3. Son olarak, ortaya çıkan uygulamanın kriptografik olarak imzalanması gerekir.
   Bu, internete bağlı olmayan bir bilgisayarda gerçekleşir. F-Droid'deki bir
   kişinin uygulamayı alıp fiziksel olarak o özel bilgisayara götürmesi gerekir.
   Bunun ne kadar süreceği, kişinin o özel bilgisayara ne sıklıkla yürüdüğüne
   bağlıdır. Genellikle, bu adım uygulama oluşturulduktan sonra 1-2 gün daha
   sürer.
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

### Beklenenden uzun sürerse ne yapabilirsiniz
Gördüğünüz gibi F-Droid'de yeni bir AntennaPod sürümünün yayınlanması bir hafta
kadar sürebilir . Bir güncelleme yayınlanmasından bir haftadan fazla süre sonra
hala yayınlanmamışsa, [forumumuzda]{1} bir gönderi oluşturarak bize bildirmekten
çekinmeyin , biz de araştıralım.

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
