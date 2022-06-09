# Audio Groups

  
![](https://gms.magecorn.com/Manual/assets/Images/Settings/Audio_Groups.png)  
The **Audio Group Manager** is available from the [Tools
Menu](../IDE_Navigation/Menus/The_Tools_Menu) in the IDE. Here you
can *add* , *delete* and *rename* **Audio Groups** , as well as set
their platform export options. GameMaker permits you to assign each of
the audio resources (sound effects and music) to different audio groups
to try and optimise the number of sounds that are being played at any
one time, as well as give you further control over what platforms they
are exported to. To define an audio group you need to click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
on the **Add New** button which will create new group that you can then
name. To change group, click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
on the drop-down menu and select the one you wish to edit. **NOTE** : If
you select streamed audio for a sound in the [Sound
Editor](../The_Asset_Editors/Sounds) , you will not be able to
assign the sound to an Audio Group as streamed sounds are not packaged
in the same way as other sounds and you have full control over when they
are loaded, played and unloaded using code. To add a sound to an audio
group, you need to open the [Sound
Editor](../The_Asset_Editors/Sounds) for that sound and then select
the group from the option you will find there, or alternatively you can
add assets to an audio group via the right mouse button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
menu in the [Asset Browser](../Introduction/The_Asset_Browser) . You
can select one or more sound assets (or an entire asset group folder)
and then use the RMB menu to add the sounds to any group. You can also
click the **Add Resource** button at the bottom of the Audio Group
Editor to add assets that way. Once you have a sound added to a custom
audio group then you can use this window to selectively choose which
platform to export that sound to. It may be that by default you have all
your sounds at the highest quality, but that for HTML5 (for example) you
want to use a lower quality sound file set to use less memory. In that
case you add the lower quality files to GameMaker and then assign them
to a new audio group. You would then select that audio group from the
drop down menu and set it to export *only* to HTML5, and remove the
HTML5 export from the higher quality audio group export options. It is
important to note that you cannot change the export options for the
"default" audio group and that it will always be exported to all
available platforms when you build a final game package. Once you have
defined audio groups and assigned sounds to them you can see them in the
list on the left when you select the group. There will always be a
"default" audio group available and all the sounds that are within this
group will always be included in the game package for all platforms and
they will all be loaded into memory on start-up (unless flagged as
"streamed" in the Sound Editor properties), but when you create a custom
audio group, the files that are added to it *will not be loaded into
memory* until you call the function [ audio_group_load()
](../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/audio_group_load)
. In this way you can control what audio is resident in memory at any
time. Note too that for all the [audio group
functions](../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/Audio_Groups)
, you will need to supply the audio group ID value. This is simply the
name that you have given the audio group. Audio Groups are also linked
to the [Configurations](Configurations) settings. When you select a
configuration, you can then open the Audio Groups window and select the
export targets from the right hand side for that configuration, and then
changing configurations will change these output targets. Note that you
cannot set sound resources to different groups on a per-configuration
basis, only the export target for the given group.
