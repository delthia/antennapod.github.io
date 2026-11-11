Voleu facilitar que la vostra xarxa o audiència incorpori el(s) teu(s)
pòdcast(s) a AntennaPod? Simplement, afegiu un enllaç com el que us és
proporcionat a sota a la vostra pàgina web o on vulgueu. Assegureu-vos de
substituir `xyz`per l'URL del vostre feed RSS i `abc` pel títol del vostre
pòdcast.

`https://antennapod.org/deeplink/subscribe?url=xyz&title=abc`

Els usuaris que hagin instal·lat AntennaPod i obrin l'enllaç podran
previsualitzar l'episodi i subscriure's al vostre pòdcast directament a l'app.
Podeu veure un exemple d'aquesta pàgina [aquí]{1}. Si necessiteu el nostre
logotip, feu una ullada al nostre [repositori de marca]{2}.

```
<style>.antennapod-subscribe{ color: #fff; background: #007bff; display: inline-block; padding: 0.5em; text-decoration:none; border-radius:0.5em; font-family: sans-serif;} .antennapod-subscribe:hover {background: #0069d9;}</style>
<a href="https://antennapod.org/deeplink/subscribe?url=xyz&title=abc" class="antennapod-subscribe">Subscribe in AntennaPod</a>
```

# What users see
Users who have installed AntennaPod and open that link will be able to preview
episodes and subscribe to your podcast directly in the app, as in the
screenshots below.

<!-- mdpo-disable -->
{% include image.html alt= "\
<!-- mdpo-enable-next-line -->\
Browser asking to open a link in AntennaPod

    "
loc="/assets/images/documentation" file="open-in-ap1.png" max-width="400px" %}

{% include image.html alt= "\
<!-- mdpo-enable-next-line -->\
The same link displayed in AntennaPod

    "
loc="/assets/images/documentation" file="open-in-ap2.png" max-width="400px" %}
<!-- mdpo-enable -->

On the other hand, users who don't have AntennaPod installed will see a page
with instructions to download the app or to subscribe to your podcast manually,
as in this [example
page](/deeplink/subscribe?url=https://antennapod.org/rss.xml&title=Blog+Posts).

# Branding
Would you like to use our logo to create a branded ‘Open in AntennaPod’ button?
You can find it in our [branding
repository](https://github.com/AntennaPod/branding).
