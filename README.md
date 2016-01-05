# CS-KickassBot
A sample bot for Cobalt Strike 3

WHAT
====

KickassBot is a tiny script written as proof-of-concept to solve one major issue. 

*What do you do when someone clicks on your phishing email and executes your beacon at 3am in the morning your local time?*

Chances are that by the time you noticed it the ~~victim~~
user has disconnected and you lost valuable evidence.

KickassBot resolves this by automating the evidence collection part by:

* Uploading and running PowerUp
* Executing "whoami /groups"
* Executing "systeminfo"
* Executing "ipconfig /all"
* Attempting to bypass UAC
* Executing mimikatz wdigest
* Taking a screenshot
* Attempting a hashdump

USAGE
=====

Assuming you have a working Cobalt Strike 3 installation you can use either "agscript" or the CS3 GUI to run .cna files. More info: https://cobaltstrike.com/aggressor-script/index.html

Recommended usage: 

    ./agscript {TeamServer_IP} {TeamServer_Port} {Nickname} {TeamServer_Pass} {location_of_KABot}/kickassbot.cna | tee output.txt