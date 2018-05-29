# Eleven

This is a fork of the LineageOS music player [Eleven](https://github.com/LineageOS/android_packages_apps_Eleven).

This version is compatible with Gradle and can simply be imported into Andriod Studio and built.
The result in a version of Eleven which works on any device starting from API level 24. Maybe I will
update it to support lower API versions (at least 21) as well in the future.

For the most part the code is the same as the original, apart from structural cahnges to support Gradle and the removal
of a few code pieces which are only available to system apps but do not influence the way the app looks and works.  
There are a few custom changes made my be however. Since this version won't be installed as a system app anymore it
is subject to restrictions added in newer Android versions. Apps now have to use Notification Channels and
several Broadcast Receivers are not allowed to be declared statically in the manifest anymore, namely the
`AUDIO_BECOMING_NOISY` one. Additionally apps are not allowed to start background services anymore while in the
background, and while the music service is a foreground service a click on the widget initially started it as a
background service.

I have been using this version daily for months by now on my phone with Android 8.0.0 and did not notice any issues
so far. It looks, feels and works exactly the same as the LineageOS-integrated version.
