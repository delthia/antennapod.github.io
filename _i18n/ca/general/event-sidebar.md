## Coneix-nos!

Us interessa en trobar-vos amb la gent que hi ha darrere d'AntennaPod? Trobareu
totes les oportunitats en aquesta pàgina!

Coneixeu un esdeveniment al vostre veinat i us agradaria trobar-vos amb
col·laboradors i usuaris d'AntennaPod? Expliqueu l'esdeveniment al nostre fòrum
per organitzar una trobada!

[Proposa una trobada](https://forum.antennapod.org)

{% assign calendar_base_url = site.data.event-links | where: 'key',
'calendar-path' | map: 'url' | first %}\
<a href="{{ calendar_base_url }}all-events" onclick="copyUrl(event);" data-bs-toggle="tooltip" data-bs-trigger="manual" data-bs-title="{% t generic.accessibility.copied %}" data-copy-url="{{ calendar_base_url }}all-events">Add
our events to your calendar</a>
