FHEM/CCU Home Cinema Service
============================

About
-----

[FHEM][1] is a GPL licensed perl server for house automation. It is used to
automate some common tasks in the household like switching lamps, shutters,
heating, etc. and to log events like temperature, humidity or power consumption.
The program runs as a server, you can control it via web or smartphone front-
ends, telnet or TCP/IP directly.

This service allows to send commands to FHEM on specific player actions in order
to create a cinema like atmosphere at home. The user can configure commands to
send to FHEM on various player events:

 - On XBMC Start
 - On XBMC Shutdown
 - On Video Playback Start
 - On Video Playback Pause
 - On Video Playback Stop
 - On Audio Playback Start
 - On Audio Playback Pause
 - On Audio Playback Stop

Optional daytime support allows to specify an alternative set of commands to use
during daylight hours.


Prerequisites
-------------

If you are using this addon with an Homematic CCU you need a system variable with a value list from 0 to 8.

For FHEM you need a working installation and knowledge about the commands to send
in order to get the desired results.

The addon communicates with FHEM using the telnet command line interface on port
7072 by default. If you have configured the telnet interface to listen on a
different port, you should adjust the port number in the addon configuration
page, where you can also specify all commands you want to be issued on player
actions. If the telnet inteface is not enabled in your FHEM configuration, you
should add the following lines to your FHEM configuration file and restart FHEM:

```
define telnetPort telnet 7072 global
```


Homematic CCU value explanation
-------------------------------

| Event                 | System variable value |
| --------------------- |----------------------:|
| XBMC start            | 1 |
| XBMC shutdown         | 2 |
| Audio playback start  | 3 |
| Video playback start  | 4 |
| Audio playback stop   | 5 |
| Video playback stop   | 6 |
| Audio playback pause  | 7 |
| Video playback pause  | 8 |
| Unknown               | 0 |


License
-------
This software is released under the [GPL 2.0 license] [2].

Useful Links
-------------

Dedicated Repository: http://archive.yeasoft.net/repository.yeasoft.zip

Support Forum: http://forum.xbmc.org/showthread.php?tid=204667


[1]: http://www.fhem.de
[2]: http://www.gnu.org/licenses/gpl-2.0.html
