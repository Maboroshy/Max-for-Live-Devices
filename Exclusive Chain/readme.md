# Exclusive Chain

One of typical use cases for Ableton Live racks is an instrument or effects path selector, when you want only one exclusive chain active at a time, with others disabled to save CPU resources. There's a [recipe](https://help.ableton.com/hc/en-us/articles/360000727359-Using-the-chain-selector-in-a-Rack) that involves mapping rack's chain selector and each device's on/off toggle to a single macro knob. 

![Preview](https://github.com/Maboroshy/Max-for-Live-Devices/blob/main/Exclusive%20Chain/Exclusive%20Chain.gif?raw=true)

My device does this without all these mappings and provides a numberbox that:
- automatically attaches to the next rack on the track or chain, any type of rack (won't be useful with a drum rack)
- selects chosen chain putting the "blue hand" on its first device
- mutes all the other chains
- enables the first device on the chosen chain (or more if you group them)
- disables the first devices on the other chains
- sends "note off" and resets sustain before changing chain

Unlike chain selector mapping recipe, you can add, remove or rearrange rack chains without needing to update any mappings.

The device also provides +/- and chain index buttons for controller mapping. There's an option for the buttons to work only while the track is armed, which allows sharing controller mappings with similar devices on other tracks. The numberbox doesn't  respect this option and will always work. The buttons can't be used while the numberbox is mapped to a controller.

The "blue hand" following chain selection can't be disabled. If you rely on the "blue hand" staying on a particular device and want to active chain selection, you'll have to disable the "Select Chain" option and use the rack's chain selector instead.

## Changelog
### v1.1 - 02.02.2026
- Fixed Exclusive Chain parameter automation
- Improved rack detection
- Silenced unwanted console messages 
