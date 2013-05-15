android-udpsender
=================

Simple application to allow sending UDP packets.  

Supports the implicit [Intent](http://developer.android.com/reference/android/content/Intent.html) *Intent.ACTION_SENDTO* with a *udp://host:port/data* format URI.  

* data is treated as hex if it starts with 0x.  
* If a string starting with 0x is to be sent it can be escaped as \0x

Tasker Integration
------------------
UDP packets can be sent via [Tasker](http://tasker.dinglisch.net/) with the Misc/Send Intent action.

Just set it up as follows:
* Action = android.intent.action.SENDTO
* Data = udp://host:port/data
* Target = Activity

Example for a www.limitlessled.com Wi-Fi bridge at 192.168.1.100 to turn on all the white LEDs
* Action = android.intent.action.SENDTO
* Data = udp://192.168.1.100:50000/0x350055
* Target = Activity

Download
--------

I hope to publish a version to the Play store in the next few days.

Meanwhile if you're happy installing from Unknown sources you can download the [UDPSender.apk](https://www.dropbox.com/s/g2lp20e17qous29/UDPSender.apk).
