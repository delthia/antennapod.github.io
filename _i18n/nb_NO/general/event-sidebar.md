## Møt oss!

Er interessert i å møte de som lager AntennaPod? Du kan se om muligheten byr seg
på denne siden!

Vet du om et arrangement i der du bor og ønsker å møte bidragsytere og brukere
av AntennaPod? Fortell oss om det på forumet slik at vi kan organisere et møte!

[Foreslå et møte](https://forum.antennapod.org)

{% assign calendar_base_url = site.data.event-links | where: 'key',
'calendar-path' | map: 'url' | first %}\
<a href="{{ calendar_base_url }}all-events" onclick="copyUrl(event);" data-bs-toggle="tooltip" data-bs-trigger="manual" data-bs-title="{% t generic.accessibility.copied %}" data-copy-url="{{ calendar_base_url }}all-events">Add
our events to your calendar</a>
