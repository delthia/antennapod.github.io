AntennaPod ile düzenli olarak güncellenecek abonelikleri (podcast yayınları)
belirtebilirsiniz (bkz. [Podcast'leri
yenileme](/documentation/automation/refreshing-podcasts)).

Daha karmaşık ihtiyaçlarınız varsa bunu yapmak için AntennaPod ile çeşitli 3.
parti otomasyon uygulamalarını kullanabilirsiniz . Örneğin:
- Aboneliklerin günün başında güncellenmesini sağlayın : sabah 7'de Wi-Fi'yi
  açın ve ardından AntennaPod yayınlarını güncelleyin .
- Aboneliklerinizi evinize gitmeden önce yaptırın : Hafta içi saat 17:00'da
  aboneliklerinizi güncelleyin .

## Genel talimatlar
Otomasyon uygulamanızda, AntennaPod'un aboneliklerini aşağıdaki ayarlarla bir
'Yayın' (bir tür Android intent olarak gösterilebilir) göndererek güncellemesini
sağlayabilirsiniz :
- Paket adı `de.danoeh.antennapod`
- Sınıf adı : ` de.danoeh.antepod.core.receiver.FeedUpdateReceiver `

## Bazı otomasyon uygulamaları için adımlar

### Automate: ([web sitesi](https://companion.home-assistant.io/docs/notifications/notification-commands/#broadcast-intent))
Bir akışta, ` APPS ` » ` Broadcast send ` türünde bir blok ekleyin ve belirtin
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

### Tasker ([website](https://llamalab.com/automate/))
Bir görev oluşturun. Görevde bir eylem ekleyin
1. `Sistemi` seçin
2. ` Gönderme Niyetini ` seçin

### Llama - Konum Profilleri ([web sitesi](https://tasker.joaoapps.com/))
Bir olay yaratın (Llama otomasyon kuralı). Olayda,
1. Android intent türünde bir eylem ekleyin.
2. İntent gönderme modunu ` Yayın ` olarak belirtin.
3. Paket adının ` de.danoeh. antennapod ` olmasını belirtin
4. Sınıf adını ` de.danoeh.antepod.core.receiver.FeedUpdateReceiver ` olarak
   belirtin
5. Özel ihtiyaçlarınıza yönelik başka koşul/eylemler ekleyin.
6. You can leave the other fields blank

---

Kısayol olarak [bu bağlantıya](http://llama.location.profiles/ AntennaPod
+feeds+Update/ AntennaPod
+feeds+Update%7C0-1-0-0-0-0-0-0-0-1-0--0-%7C%3A%7Ct%7C420%7C425%7Cai%7Cde.danoeh.
antennapod tıklayabilirsiniz
%7CFgAAAGEAbgBkAHIAbwBpAGQALgBjAG8AbgB0AGUAbgB0AC4ASQBuAHQAZQBuAHQAAAAAAP%2F%2F%2F%2F%2F8AAAAA%2F%2F%2F%2F%2FwAAAAD%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FxQAAABkAGUALgBkAGEAbgBvAGUAaAAuAGEAbgB0AGUAbgBuAGEAcABvAGQAAAAAADU
Başlamak için örnek bir olay oluşturmak üzere
AAABkAGUALgBkAGEAbgBvAGUAaAAuAGEAbgB0AGUAbgBuAGEAcABvAGQALgBjAG8AcgBlAC4AcgBlAGMAZQBpAHYAZQByAC4ARgBlAGUAZABVAHAAZABhAHQAZQBSAGUAYwBlAGkAdgBlAHIAAAAAAAAAAAAAAAAAAAAAAAAAAA%2Fv%2F%2F%2F%2F%2F%2F%2F%2F8%3D%7C2%7C)
komutunu kullanın.
