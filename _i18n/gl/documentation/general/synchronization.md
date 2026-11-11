<!-- mdpo-disable -->

{% capture img-devices %} {% include image.html alt="

    dispositivos

       "
loc="/assets/images/documentation" file="gpodder-devices.png" %} {% endcapture
%}

{% capture img-synchronize %} {% include image.html alt="

    dispositivos

       "
loc="/assets/images/documentation" file="gpodder-synchronize.png" %} {%
endcapture %}

<!-- mdpo-enable -->

AntennaPod pode sincronizar as túas subscricións e o progreso de escoita con
outras instalacións de AntennaPod, así como con outras aplicacións (de
escritorio). Para configurar a sincronización, necesitas un servidor, o punto
central a través do cal os teus datos compártense con outros dispositivos. Tes
varias opcións para isto:

* [gpodder.net](https://gpodder.net/) ofrece un servidor de sincronización
  gPodder gratuíto ao que **calquera pode unirse**. Desafortunadamente, debido á
  popularidade do servizo e o seu financiamiento limitado, este servidor a miúdo
  está sobrecargado, o que xera erros en AntennaPod.
* Recoméndase encarecidamente aos usuarios máis inclinados á tecnoloxía que
  **autohospeden un servidor de sincronización**. Un servidor autohospedado é
  máis confiable e axuda a reducir a carga dos servizos públicos gratuítos. Hai
  varias opcións: [Nextcloud]{1} coa [aplicación gPodder Sync]{2}, unha [
  gPodder]{3}, ou o [servidor Micro GPodder]{4}.
  * [Nextcloud](https://nextcloud.com/install/#instructions-server) with the
    [gPodder Sync app](https://apps.nextcloud.com/apps/gpoddersync) (PHP)
  * [oPodSync](https://github.com/kd2org/opodsync) (PHP)
  * [goPodder](https://github.com/cbrgm/gopodder) (Go)
  * [podsync](https://github.com/bobrippling/podsync) (Rust)
  * [malipod](https://github.com/eliassoares/malipod-selfhosted) (Python)

These are third-party projects not affiliated with AntennaPod.


## Activa a sincronización a través de Nextcloud
1. Se tes unha conta de Nextcloud, instala a aplicación gPodder Sync ou solicita
   ao administrador do servidor que o faga
2. Ve a `Configuración` » `Sincronización` en AntennaPod e toca `Seleccionar un
   provedor de sincronización`
3. Selecciona 'Nextcloud'
4. Ingresa a 'Server address' (a URL ou a dirección IP do servidor) e toca
   `Proceed`
5. Inicia sesión na xanela do navegador que se abre e autoriza a AntennaPod

## Habilitar a sincronización a través de gPodder
1. Crea unha conta no servidor www.gpodder.net ou no teu propio servidor
2. When you have an account, log in on the webserver and create a device under
   `Subscriptions` » `Devices` for each client that you use:{1}{{ img-devices |
   strip }}
   <!-- mdpo-disable-next-line -->
   <br />{{ img-devices | strip }}
3. When you have added the devices to your account, link them using the
   "Configure" button. This way, gpodder.net automatically keeps the activated
   devices synchronized.{1}{{ img-synchronize | strip }}
   <!-- mdpo-disable-next-line -->
   <br />{{ img-synchronize | strip }}
4. Ve a `Configuración` » `Sincronización` en AntennaPod e toca `Seleccionar un
   provedor de sincronización`
5. Seleccione 'gPodder'
6. Introduza a dirección do servidor (por exemplo, www.gpodder.net) e pulse
   `Iniciar sesión`
7. Introduza o "Nome de usuario" e o "Contrasinal" e pulse `Iniciar sesión`
8. Seleccione o dispositivo que creou no servidor

**Nota** Creou un dispositivo mentres configuraba a sincronización en AntennaPod
en lugar de crear un dispositivo de antemán no sitio web? Así que asegúrache de
presionar o botón `Force sync` en AntennaPod para cargar o modo de reprodución
de todos os episodios que escoitou no pasado. Se non fas isto, só
sincronizaranse os podcasts que se agregaron *despois** de vincular os
dispositivos. Hai un [problema aberto para
gpodder.net](https://github.com/gpodder/mygpo/issues/388) que solicita cambiar
este comportamento.
