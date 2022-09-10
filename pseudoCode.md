# How to brew a cup of tea
## ABOUT: 
### These instructions will list the basic steps needed to brew a cup of tea with a kettle.
### Tea can either be a calming effect or caffienated depending on the leaves used.
### To infuse the hot water with tea, a prepackaged  satchel or loose leaf in a metal mesh containter

#### ASSUMED: Access to water, stovetop/microwave, tea leaves, cup, and basic physical dexterity 

## INTIALIZE 
### kettle
#### &emsp; -Holds the water to be heated
#### &emsp; -Will be used if stovetopBurner exists
#### &emsp; Properties
#### &emsp; &emsp; kettle.Water
#### &emsp; &emsp; kettle.Sprout
### teaPacket
#### &emsp; -Can either be loose tea leaves or prepackaged 
#### &emsp; -In this insance a prepackaged will be used 
#### &emsp;  Properties
#### &emsp; &emsp; teaPacket.Satchel
### faucet
#### &emsp; -dispenses water into the kettle/cup
#### Properties
#### &emsp; &emsp; faucet.Location
### cup
#### &emsp; -Will hold the final product
#### &emsp; Porperties
#### &emsp; &emsp; cup.Location
### spoon
#### &emsp; -Used to mix the tea mixture for an even taste
 stovetopBurner, microwave, counter, trashCan, taste, sugar, milk

## OPEN teaPacket
&emsp;

## IF stovetopBurner exists {
### PLACE teaPacket.satchel in cup
### PLACE cup on counter
### IF no measurement exists fill kettle for approximatly 3 seconds.
### ELSE FILL kettle with 400mL of water from faucet
### PLACE kettle on stovetopBurner
### LIGHT stovetopBurner, adjust to medium heat
### IF kettle.whistle exists 
##### LISTEN for kettle.whistle
### ELSE
##### TIME kettle for 3 minutes
### TURNOFF stovetopBurner
### PICKUP kettle from the handle
### POUR kettle.water into cup to fill up to the brim of cup
### PLACE kettle onto stovetopBurner
### }

## ELSE stovetopBurner does not exist {
### FILL cup from faucet with water to desired drinking amount
### PLACE cup in microwave
### SET microwave for 2 minutes
### START microwave
### REMOVE cup from microwave and place on counter
### PLACE teaPacket.satchel in cup
### } 

## WAIT 2 minutes
## REMOVE teaPacket.satchel
## PLACE teaPackect.satchel into trashCan
## IF taste is sweet
#### ADD sugar to cup
## IF taste is creamy
#### ADD milk to cup
## STIR with spoon
## REMOVE spoon
## DRINK tea
## REALIZE tea is just hot brown water

