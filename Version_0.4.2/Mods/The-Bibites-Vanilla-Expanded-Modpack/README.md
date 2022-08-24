# The-Bibites-Vanilla-Expanded-Modpack
A Modpack for the Bibites containing Mods which could be resonably added to the base game. 

Activating/deactivating mods and changing their settings can be done in the config.txt file in the games Mods folder

## Instalation Guide
1) make a backup save of your Bibites folder somehwere
2) download the zip file and unzip it somewhere
3) drag the "The Bibites_Data" folder into your Bibites folder. If it asks you, if you want to replace files, you confirm that. 

## Mods Included

### Neurons Plus: 
This mod adds 4 new activation functions for neurons, most notably the highly suggested multiplication neuron:
1) Mult: Multiplies all inputs together
2) Div: Divides 1 by the sum of inputs
3) Ln: Takes the natural logarithm of the sum of inputs
4) Exp: Exponentiates Euler’s number e by the sum of inputs 

### Senses Plus: 
This mod adds 6 new input neurons generally related to sensing:
1) Rotation Speed: Lets the Bibite sense its rotation speed
2) Bibite Heading Angle: Lets the BIbite see the direction Bibites in view are moving towards.
3) Target Diet: Lets the Bibite see the diet gene of the closes Bibite.
4) Target Speed: Lets the BIbite see the speed the closes Bibite is moving at.
5) Target Size: : Lets the BIbite see the size of the closes Bibite.
6) Own Red, Green and Blue letting the Bibite sense the red, green and blue components of its own color .

### YBKs Vision Rework Mod:
This Mod implements the Vision Rework suggested by YBK and Leo’s addition to it. It adds 3 output neurons controlling the vison of the Bibite:
1) Field Of View: A multiplier by which the View Angle Gene is multiplied to determine the real View Angle
2) Panning: The amount by which the Vision Cone is angled to the left/right of center
3) Range Of View: A multiplier by which the View Range Gene is multiplied to determine the real View Range

This Mod has one further configuration. If DefaultMultiplyerIsOne is true (which it is by default) Field of View and Range of View will be 1 if there are no inputs going into it. If it is false, the multipliers will be 0.5 if there are no inputs. 

### Better Initial Connections:
This Mod aims to change the Helpful Initial Connections Option to get a stable population of Bibites quicker:
1) unchanged. Links Constant to Accelerate and gives a minimally adapted stomach
2) unchanged. Links a Food Angle to Rotate
3) Links Energy Ratio to Growth. Also makes a random connection either through a neuron or through pheromones 
4) Links Constant to Grab. 
5) Makes 3 random connections. Those might be through a neuron or pheromones. 

This Mod has one further configuration. If No Aggressive Virgins is true (which it is by deafult) No virgins will spawn with their Bibite Angle Neuron being connected to rotate. 

