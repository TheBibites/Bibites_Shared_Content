# Constance-Mod
A Mod for the artificial life game ["The Bibites"](https://leocaussan.itch.io/the-bibites)

### What is this Mod about
The Constance Mod is about fixing certain genes of a Bibite, certain neurons and certain synapses and preventing all mutations that would affect those genes, neurons and synapses. It also has the secondary functionalities of changing traits (genes, synapses, neurons) of all Bibites in a world, giving access to the value of a Bibites genes to the neural network brain of the Bibite, and providing extended functionalities of the [Dummy Tag Mod](https://github.com/Conni243/DTMod). <br /><br />

## Installation Guide
How to install the Constance Mod: 
1)	Make a Backup of your Bibite game folder.
2)	Download the zip file of the mod
3)	Unpack the zip file somewhere
4) Take the file *BibitesAssembly.dll* and drop it into *[your Bibite folder]\The Bibites_Data\Managed*. When Windows asks you, if you want to replace the file, you click yes. <br /><br />

## Use Guide
How to make the Constance Mod fix what you want. 
1)	Take the .bb8 file of the Bibite you want to be affected and drop it into *[your Bibite folder]\The Bibites_Data\Mods*. Note: it’s not the filename by which it is determined, whether a Bibite will be affected, but by the tag, the .bb8 file has. All Bibite of that tag will be affected. You should not put multiple .bb8 files with the same tag into the Mods folder
2)	Open the .bb8 file in the Mod folder in your file editor of choice. I recommend Visual Studio as it can format the .bb8 file into something more readable, if you didn’t check the Format JSON tick box when saving the Bibite
3)	Remove all genes, neurons and synapses, which you *DO NOT* want to keep constant. *All* remaining  genes, neurons (*including* Input and Output Neurons) and synapses will be kept constant. You may also only delete certain attributes  of neurons (Type) and synapses (Weight, En status) to allow that certain attribute to mutate, but still disallow  other attributes to change and that neuron or synapse to be removed. 
4)	Load the game or a Bibite world. This is the only way to load your configured .bb8 file to have effect.<br /><br />

## Additional Information on Constance
A Constant synapse will not be deleted or split into two to form a neuron. A Constant Synapse will also not change its weight and not be toggled on/off, if those attributes are present in the configured .bb8 file. <br /><br />
A Constant neuron will not be removed and will not have new synapses be created with it as its output. This is to prevent the degradation of complex brain structures. A Constant Synapse will also not change its Type, if this attribute is resent in the configured .bb8 file. <br /><br />
A non-constant neuron will not be removed if it would lead a constant synapse to be removed <br /><br />

## Feature 2: Globally change  Bibites Attributes
If a trait of a newly hatched  Bibite (a gene, synapse, neuron) is different to the present trait in the configured .bb8 file, it will be set to be the same as in the configured .bb8 file. If a synapse or neuron is present in the configured .bb8 file, but not in the newly hatched Bibite, that synapse or neuron will be generated. <br /><br />
This solves a problem of the  hybrid approach between evolving and engineering a Bibite, where you would pick out a single individual from a population to make changes to it and let it be the sole seed of a new population. The old method has the problem of killing off any existing biodiversity and has the potential to cause evolutinary setbacks, if that chosen individual happened to have detrimental mutations. <br /><br />
## Feature 3: Brain Access to Bibite Genes
If the weight of a synapse in the configured .bb8 file is a whole number surrounded  by quotation marks, that synapses weight will be equal to the value of one of the Bibite's genes. Which number correspond to what gene can be found out in the "neuron and gene indexes" text file included file in this folder. <br /><br />
Connecting a synapse with weight of a gene from the constant neuron to a linear neuron makes that neuron basically a pseudo input node with value of that gene. <br /><br />
This is especially useful for predators  and aggressive herbivores. If your Bibite seeks out other Bibites to kill, it is useful for it to distinguish closely related Bibites from foreign Bibites. A Bibite can do this by comparing the difference  of the red, green and blue color components of itself with the Bibite it sees and only enabling  aggresive behaviors  towards it, if their color is dissimilar  enough.<br /><br />
But of course, it has its other uses. <br /><br />

## Feature 4: Extended Dummy Tag Mod
Dummy Tag Mod is a mod developed by @Conni243. It was developed to add new evolutinary forces to Bibites who live in a world where some scenarios are not possible. This new version of the Constance Mod extend the functionality of the Dummy tag Mod by providing more options and more customizability. <br /><br />
Dummy Tag mode is activated for Bibites, that have the string ".dummy" in their tag. While in regular mode the Constance Mod only allows you to keep genetic attributes  like genes, neurons and synapses constant, in Dummy tag mode you can make live attributes  constant. Those live attributes are: stomach contents, health, energy, d2Size, the ability to dying or stay immortal of dying is set to false, maturity and time alive. All live settings that are present will be constant if Dummy Tag mode is active, remove all live traits that you do not want to stay constant. If Dummy Tag mode is active for a Bibite, it will also have void no more active. <br /><br />
Note that having health constant does not make the Bibite immortal. It can still die, if one hit brings it to 0 health. If you want your Bibite to be immortal set dying to false. The only way to kill a Bibite with dying set to false it to rename it, so Constance Mod has no effect on it anymore <br /><br /><br />

#### Ps
All bugfixes that are currently on my [Bibites-Quickfixes repo](https://github.com/YBKy/Bibites-Quickfixes) are also implemented here
