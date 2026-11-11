## Bizimle tanış!

AntennaPod'un arkasındaki insanlarla tanışmak ister misiniz? Tüm fırsatları bu
sayfada bulabilirsiniz!

­Mahallenizde bir etkinlik olduğunu biliyor musunuz ve AntennaPod katılımcıları
ve kullanıcılarıyla buluşmak mı istiyorsunuz? Bir buluşma düzenlemek için
forumumuzdaki etkinlikten bahsedin!

[Bir buluşma önerin](https://forum.antennapod.org)

{% assign calendar_base_url = site.data.event-links | where: 'key',
'calendar-path' | map: 'url' | first %}\
<a href="{{ calendar_base_url }}all-events" onclick="copyUrl(event);" data-bs-toggle="tooltip" data-bs-trigger="manual" data-bs-title="{% t generic.accessibility.copied %}" data-copy-url="{{ calendar_base_url }}all-events">Add
our events to your calendar</a>
