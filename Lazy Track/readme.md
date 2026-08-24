# Lazy Track

Disables all devices on a track when there's no output and input, saving CPU resources. New input re-enables devices. 

![Preview](https://github.com/Maboroshy/Max-for-Live-Devices/blob/main/Lazy%20Track/Lazy%20Track.gif?raw=true)

Re-enabling MIDI input is resent with a short delay to go through enabled devices.

Works for both audio and MIDI tracks. 

When placed in a rack, it disables all devices in the chain it's placed in. 

There are limitations: 
- Visible track volume mixer required to observe track's output level. 
- The audio version observes MIDI input only while the track is selected - use the MIDI version instead. 
