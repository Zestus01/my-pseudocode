# How to brew a cup of tea
## ABOUT: 
### These instructions will list the basic steps needed to brew a cup of tea with a kettle.
### Tea can either be a calming effect or caffienated depending on the leaves used.
### To infuse the hot water with tea, a prepackaged  satchel or loose leaf in a metal mesh containter
&emsp;
#### ASSUMED: Access to water, stovetop/microwave, tea packet, cup, basic physical dexterity, and immunity to heat.
##### &emsp;
## INTIALIZE 
### kettle
#### &emsp; -Holds the water to be heated
#### &emsp; -Will be used if stovetopBurner exists
#### &emsp; Properties
#### &emsp; &emsp; kettle.Water
#### &emsp; &emsp; kettle.Sprout
#### &emsp; &emsp; kettle.Top
### teaPacket
#### &emsp; -Can either be loose tea leaves or prepackaged 
#### &emsp; -In this insance a prepackaged will be used 
#### &emsp;  Properties
#### &emsp; &emsp; teaPacket.Satchel
### faucet
#### &emsp; -dispenses water into the kettle/cup
#### &emsp; -Starts with infinite Water
#### Properties
#### &emsp; &emsp; faucet.Location
#### &emsp; &emsp; faucet.Water 
### cup
#### &emsp; -Will hold the final product
#### &emsp; Porperties
#### &emsp; &emsp; cup.Location
### spoon
#### &emsp; -Used to mix the tea mixture for an even taste
#### Properties 
#### &emsp; &emsp; -spoon.Stir
### stovetopBurner
#### &emsp; -Used to heat up the kettle
#### &emsp; -Has 4 heat settings; High, medium, low, and off
#### &emsp; Properties
#### &emsp; &emsp; stovetopBurner.Heat
#### &emsp; &emsp; stovetopBurner.Loctation
#### &emsp; &emsp; stovetopBurner.Exists
### microwave
#### &emsp; -Will be uses to heat up the water directly in the cup if stovetopBurner doesn't exists
#### &emsp; -No heat setting, only on or off
#### &emsp; Properties
#### &emsp; &emsp; microwave.Location
#### &emsp; &emsp; microwave.Time
### counter
#### &emsp; -Used to for a flat surface to hold objects
#### &emsp; -Not generally heat resistant, but in this case it is not being afftected by the heat from the hot kettle 
#### &emsp; Properties
#### &emsp; &emsp; counter.Location
### trashcan
#### &emsp; -A waster holder
#### &emsp; -Used for throwing things away
#### &emsp; Properties
#### &emsp; &emsp; trashcan.Location
### taste
#### &emsp; -Each property is a boolean
#### &emsp; Properties
#### &emsp; &emsp; taste.Sweet 
#### &emsp; &emsp; taste.Creamy
#### &emsp; &emsp; taste.Honey
#### &emsp; &emsp; taste.Calm
### &emsp;

## Functionality
### PLACE (object1, object2)
#### &emsp; Given two objects and places object1 onto object2
### POUR (object1, object2)
#### &emsp; Sets object2.Water to object1.Water
#### &emsp; Sets object1.Water to 0
### LIGHT (object, state)
#### &emsp; Changes object to given state
### TIME (number)
#### &emsp; Sets a delay in the process for number amount
### LISTEN (object)
#### &emsp; Runs a while loop until object makes a noise
#### &emsp; Checking if kettle.Whistle becomes true
### STIR 
#### &emsp; Places spoon into cup
#### &emsp; Runs a loop moving spoon position in small circles
#### &emsp; Places spoon onto counter
### &emsp;
## START
### IF stovetopBurner is true {
#### &emsp; PLACE kettle under faucet     
#### &emsp; POUR faucet into kettle
#### &emsp; PLACE kettle on stovetopBurner
#### &emsp; LIGHT stovetopBurner, adjust to medium heat
#### &emsp; IF kettle.whistle exists 
##### &emsp; &emsp; LISTEN kettle.Whistle
#### &emsp; ELSE
##### &emsp; &emsp; TIME kettle for 3 minutes
#### &emsp; LIGHT stovetopBurner to off
#### &emsp; PLACE kettle.Sprout over cup
#### &emsp; POUR kettle.Water into cup to fill up to the brim of cup
#### &emsp; PLACE kettle onto stovetopBurner
#### &emsp; }
### &emsp;

### ELSE stovetopBurner is false {
#### &emsp; FILL cup from faucet with water to desired drinking amount
#### &emsp; PLACE cup in microwave
#### &emsp; LIGHT microwave to on 
#### &emsp; TIME microwave for 2 minutes
#### &emsp; LIGHT microwave to off
#### &emsp; PLACE cup put on counter
####  &emsp;} 
#### &emsp;
### OPEN teaPacket
### PLACE teaPacket.satchel in cup
### PLACE teaPacket in garbageCan
### TIME 2 minutes
### PLACE teaPackect.satchel into trashcan
### IF taste.Sweet
#### &emsp; PLACE sugar into cup
### IF taste.Creamy
#### &emsp; PLACE milk into cup
### IF taste.Honey
#### &emsp; PLACE honey into cup
### STIR with spoon
### DRINK tea
### REALIZE tea is just hot brown water
## End
