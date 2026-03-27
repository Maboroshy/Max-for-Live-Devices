# Retro Rec

I wanted a device like this each time I messed up a loop recording.

When you mess up, you have to finish the record, delete the clip and start recording a new one, hoping you get it right this time. Annoying when your do it live. 

With this device you just play and hit save button only once, when you know it sounds right. It saves the number of played bars you set. 

Here is what it does in detail:
1. When transport is running and track is armed, the device starts recording to a temp clip. It always record what you play. The recording follows scene selection. Manually started clip recording is also treated as a temp clip. 
2. The "Save" buttons save the selected number of last played bars as a permanent clip. At the end of the bar where you release the button the device trims the clip and starts playing it. 
3. MIDI notes played a bit too early (within a set timing margin) get shifted into the saved bars.
4. An unsaved temp clip is deleted when track is unarmed or its recording stops. 

The actions above can be disabled individually. You can use only manually started clip recording. 

These actions take some time, somewhere between 100 ms and 200 ms on my system. If they started after clip record ending they would swallow the first notes of the clip playback. The "Saving Offset" setting solves that by starting the actions slightly before the record ending. You can tune this setting for your system, but make sure to have a safety margin. Clip trimming happens in UI thread, so it's affected by CPU overload. 

The device only affects the track it is placed on, so you can use different options for each track. Add the device to each track you want to retro record. Save buttons on devices on different tracks can share controller mappings. Devices on unarmed tracks won't react to the buttons. 

The device enforces and uses "1 bar" global launch quantization and cannot be automated.

It by is also hosted with on GitHub with my other free devices:  
[https://github.com/Maboroshy/Max-for-Live-Devices/](https://github.com/Maboroshy/Max-for-Live-Devices/)

Licensed under the GNU Lesser General Public License v3.0 (LGPL‑3.0).
