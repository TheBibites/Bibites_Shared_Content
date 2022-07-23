# Constance-Mod
A Mod for the artificial life game ["The Bibites"](https://leocaussan.itch.io/the-bibites)


To all my fellow Bibite engineers, I ask you this: have you ever created a complex brain structure, just for the sands of time and random mutations to slowly wither away at your creation? Have you ever created a behavior that relied on a specific trait of the Bibite (like its color for freind/foe distinction), but random mutations changed it beyond recognition? Well, I have the solution for you: the Constance Mod! <br /><br />

### What is this Mod about
The Constance Mod is about fixing certain traits of a Bibite, certain neurons and certain synapses and preventing all mutations that would affect those traits, neurons and synapses. It also has the secondary functionality of changing traits (not currently neurons and synapses) of all BIbites in a world. <br /><br />

## Installation Guide
How to install the Constance Mod: 
1)	Make a Backup of your Bibite game folder. 
2) Take the file *BibitesAssembly.dll* from this Constance Mod folder and drop it into *[your Bibite folder]\The Bibites_Data\Managed*. When Windows asks you, if you want to replace the file, you click yes. Doesn't work on mac 

## Use Guide
How to make the Constance Mod fix what you want. 
1)	Take the .bb8 file of the Bibite you want to be affected and drop it into *[your Bibite folder]\The Bibites_Data\Mods*. Note: it’s not the filename by which it is determined, whether a Bibite will be affected, but by the tag, the .bb8 file has. All Bibite of that tag will be affected. You should not put multiple .bb8 files with the same tag into the Mods folder
2)	Open the .bb8 file in the Mod folder in your file editor of choice. I recommend Visual Studio as it can format the .bb8 file into something more readable, if you didn’t check the Format JSON tick box when saving the Bibite
3)	Remove all genes, neurons and synapses, which you DO NOT want to keep constant. All other genes, neurons (with the exception of Input and Output Neurons) and synapses will be kept constant. 
4)	Load a Bibite world. This is the only way to load your configured .bb8 file to have effect. If you changed the file while running a simulation, just save it and load it. I don’t think quick save and quick load and auto save and auto reload will work. 

## Additional Information
The genetic traits of the Bibite will be set to those in the config .bb8 file in the Mods folder open birth. It does not affect the genetic traits of currently alive Bibite's. <br /><br />
A Constant synapse will not: change weight, be toggled on/off, be removed, be split into two to form a neuron. <br /><br />
A constant neuron will not: change type, be removed. It also doesn’t allow new synapses to be formed that have that neuron as the output neuron. That is a measure to prevent the degradation of complex structures. If you want a constant neuron that can still get new input synapses, you’ll have to use a workaround. Create a new non-constant neuron and have it feed into the constant neuron with a constant synapse. <br /><br />
A non-constant neuron will not: be removed if it would lead a constant synapse to be removed
