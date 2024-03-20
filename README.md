Block TCP matches.
Shared in channel  https://t.me/efootballCheaterReport 

and group https://t.me/eFootballxjbt 

Origin:  https://t.me/efootballCheaterReport/159

In eFootball , Konami provides three modes: peer-peer as previous PES, Peer-Server-Peer via UDP and Peer-Server-Peer via TCP. The TCP one is the most laggy. It makes people feel unplayable. So the first thing you start to play the game online is to block TCP matches.

The principle of blocking TCP matches is to block access to the server-side TCP ports 30000-35000. Steam or MS store users can do it on PC’s firewall, other users need to do it on router.

Here is how PC users configure.

Right click start button. Start a terminal as administrator

Modify the CMD below with correct directory and run it in the terminal..   For steam user :
>netsh advfirewall firewall add rule name="eFootballnmt" program="D:\SteamLibrary\steamapps\common\eFootball\eFootball\Binaries\Win64\eFootball.exe" protocol=tcp remoteport=30000-35000 dir=out action=block

For MS store user:
>netsh advfirewall firewall add rule name="eFootballnmt-MS" program="D:\XboxGames\eFootball™ 2024\Content\PesConsole\console_wgd_PesShipping\Master\PesConsole-Shipping_console_wgd_Master.exe" protocol=tcp remoteport=30000-35000 dir=out action=block

It will create a rule in “windows defenders firewall with advanced security”. You can manage it as well.


This Method can also be used to block bad servers Here is the cmd
For Steam user:
>netsh advfirewall firewall add rule name="eFootballbadserver" program="D:\SteamLibrary\steamapps\common\eFootball\eFootball\Binaries\Win64\eFootball.exe" remoteip=34.92.0.0/16,34.150.0.0/16 protocol=udp remoteport=30000-35000  dir=out action=block

For MS store user:
>netsh advfirewall firewall add rule name="eFootballbadserver-MS" program="D:\XboxGames\eFootball™ 2024\Content\PesConsole\console_wgd_PesShipping\Master\PesConsole-Shipping_console_wgd_Master.exe"  remoteip=34.92.0.0/16,34.150.0.0/16 protocol=udp remoteport=30000-35000  dir=out action=block
