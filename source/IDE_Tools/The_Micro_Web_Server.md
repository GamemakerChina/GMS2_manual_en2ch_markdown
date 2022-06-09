# The Micro Web Server

This small tool's primary function is to connect to and serve files to
some of the available target platforms for GameMaker (like the HTML5
target). It also serves files for the GameMaker manual when used
offline. When you run a game on a target that requires the Micro Web
Server, you will see a new window open as the game is served to the
chosen device:  
![](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Micro_Web_Server.png)  
NOTE The first time you run a game on a target that requires the Micro
Web Server, you may get a firewall alert. You should permit the web
server to communicate through the firewall if this happens. When the
Micro Web Server is running, you can access your game from any local
device (and even remotely, if port forwarding is properly set up).
Simply access your computer's local IP address through the port shown in
this window, and you will be able to play your game from another device,
like a mobile phone, or another computer. For example, let's say your
computer's local IP address is 192.168.0.110 ( [read
this](https://lifehacker.com/how-to-find-your-local-and-external-ip-address-5833108)
to know how to find it), and the port shown in the Micro Web Server
window is 51264 . After running the game on your computer, you would
connect to 192.168.0.110:51264 from a browser on your mobile, and play
your game. The Web Server will show a certain amount of debug
information related to the files that have been served, and has a button
to clear this at the bottom. Beside the "Clear" button is the path to
the root JS file for the project, while underneath that you have the
**Network Speed** option. This is set to "No Limit" by default, but
clicking it will open up a list of different network options:  
![](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Micro_Web_Server_Bandwidths.png)  
Changing this setting will also change the package **Size** option to
the right. You can also edit this manually, in which case the Network
Speed will be set to "Custom". Setting it to anything other than the
maximum value will effectively throttle the network transfer speed and
permit you to test games in a low bandwidth environment. You can also
see the list of **Allowed IPs** along with the **Port** number being
used, but these cannot be edited in the Micro Web Server. They should be
set instead in the [Device
Manager](../Setting_Up_And_Version_Information/The_Device_Manager)
settings for the given device target, or the
[HTML5 Preferences](../Setting_Up_And_Version_Information/Platform_Preferences/HTML5#h)
when using the "Default" device.
