# rm-notifier-public
Browse documentation and report issues regarding RM-Notifier.

# About RM-Notifier

RM-Notifier is an unofficial tool to help you stay up to date with your favourite streams and DJs on RauteMusik.
When you subscribe a DJ or an entire stream you will be notified via a push notification whenever they go live!

Although this app is made possible through the use of RauteMusik's API, it should by no means be viewed as an official app of the platform.
I currently am an active member of RauteMusik but at this point in time, this is nothing more than a personal project of mine.

If you encounter any problems, feel free to message us here:
contact@rm-notifier.com

# Documentation

In this section I would just like to clear up some things that might be confusing for new users.

## Subscriptions & Initial setup
Upon opening the app for the first time, you will be greeted with a text similar to the description on this page.
After that you'll be greeted by a list of streams to choose from. These are all of the moderated RauteMusik channels you may subscribe to.
Once you confirm this dialog you'll be greeted with all the DJs that are currently in my database. 
Due to the high number of DJs, this dialogue contains a filter function for convenience. 

If you are not interested in subscribing to either category, you may confirm a dialog with an empty selection.
But please do keep in mind that selecting neither >=1 stream OR DJ will render the app completely useless.
Of course all of your subscriptions can be edited later.

If you subscribe to a stream, you will subscribe to every show on this stream, regardless of the DJ.
If you subscribe to a DJ, you will subscribe to every show by this DJ, regardless of stream.

> Technically speaking you could say that your DJ and stream subscriptions are (inclusive) OR connected.

## Upcoming & Live shows
After the initial setup is complete, you will be greeted with buttons to edit your Stream and DJ selections as well as two tabs `Live` and `Upcoming`.
The `Live` tab will display all shows that are currently live (based on your subscriptions).
The `Upcoming` tab will display the next 7 days worth of shows, based on your selection.
Due to some technical limitations the information in the `upcoming` tab may be out of date by ~(x * 3min) (x being the number of moderated RauteMusik streams.
At the time of writing this amounts to about 69 minutes of potential delay. 

## Syncing
Sometimes new streams emerge and even more often than that, new DJs join or leave the platform.
In order to present you the most up to date information, the app will automatically synchronise with the server every 7 days (when opened). 
If you would like to trigger a sync manually, you may use the Sync button at the top. 

On the serverside streams are synchronised every 7 days with the RauteMusik database.
DJs are synced every Monday morning.

## Notifications
By far the most important aspect of the RM-Notifier are the notifications.
A notification gets sent as soon as a show starts. 
The app then receives a Push Notification. 
This type of message is sent from a server directly to the app on your phone.

## Technical details
Here are some technical details for the curious:

* app and server software are both written in Kotlin
* server software is a Spring Boot Application running in the cloud
* subscriptions & notifications are handled through Firebase Cloud Messaging
