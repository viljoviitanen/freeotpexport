# freeotp-export

FreeOTP qrcode exporter app in javascript

Backround: FreeOTP is a Google Authenticator compatible open source Android app, made by Red Hat. Available at https://play.google.com/store/apps/details?id=org.fedorahosted.freeotp .

Google authenticator does not allow backuping the secrets with adb, to backup one needs a rooted phone. FreeOTP however allows adb backup. The backup file obviously can be restored to any android phone, but for easy transfer to other phones, you can create qrcodes with this app. The app does all processing locally, no data is sent anywhere (this is easy to verify with browser developer tools, also the main source of the app is pretty simple, most of the code is in third party libraries).

__Be sure to understand the security implications of backing up the secrets from the authenticator app, and writing them on your computer storage.__

# Instructions

Make an adb backup of FreeOTP, (details on how to do this are currenly left as an excercise for the reader. While you are doing the backup, consider the above warning!). Open the adb backup file (.ab) with this app. Read the displayed qrcodes with the authenticator app on your other phone.

The author has tested the app with current Google Chrome and Mozilla Firefox on Ubuntu 16.04 in April 2017. Other browsers probably do not work. Generated qrcodes have been succesfully imported in FreeOTP and Google Authenticator on Android and Microsoft Authenticator on Windows Phone 8, Windows Phone 10 and Android.

This app can be opened directly at https://rawgit.com/viljoviitanen/freeotp-export/master/export.html

![QR Code to App](qr_code.png "QR Code to App")

# Acknowledgements

Based on https://github.com/philipsharp/FreeOTPDecoder (Apache license)

Uses https://github.com/davidshimjs/qrcodejs (MIT license)

Uses https://github.com/nodeca/pako (MIT license)

Uses https://github.com/Qvazar/js-untar (MIT license)

Content is served by https://rawgit.com/

# License

Apache License, Version 2.0
