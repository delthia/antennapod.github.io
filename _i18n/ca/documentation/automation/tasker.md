Amb AntennaPod, podeu especificar subscripcions (fonts de pòdcasts) que
s'actualitzen automàticament (veieu [Actualitzar
pòdcasts](/documentation/automation/refreshing-podcasts)).

If you have more complex needs, you can use various 3rd-party automation
applications with AntennaPod to do so. For example:
- Get the subscriptions updated at the start of the day: at 7am, switch on WiFi,
  then update AntennaPod feeds.
- Get your subscriptions before your ride home: at 5pm on weekdays update
  subscriptions.

## General instructions
In your automation application, you can get AntennaPod to update its
subscriptions by sending a 'Broadcast' (it may be shown as a type of Android
intent) with the following settings:
- Package name: `de.danoeh.antennapod`
- Class name:
  `de.danoeh.antennapod.net.download.service.feed.FeedUpdateReceiver`

## Steps for some automation apps

### Automate ([website](https://companion.home-assistant.io/docs/notifications/notification-commands/#broadcast-intent))
In a flow, add a block of the type `APPS` » `Broadcast send` and specify
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
Create a task. In the task, add an action
1. Select `System`
2. Select `Send Intent`

### Llama - Location Profiles ([website](https://tasker.joaoapps.com/))
Create an event (Llama automation rule). In the event,
1. Add an action of type Android intent.
2. Specify Intent send mode to be `Broadcast`.
3. Specify Package name to be `de.danoeh.antennapod`
4. Specify Class name to be
   `de.danoeh.antennapod.net.download.service.feed.FeedUpdateReceiver`
5. Add any other condition / actions for your specific needs.
6. You can leave the other fields blank

---

As a shortcut, you can click [this link]{1} to create an example event to get
started.
