# SimplifiedAttributes
Made an tested with SkBee 2.7.1+  
You can find attribute names, slot names, value limits, operations (here](https://minecraft.fandom.com/wiki/Attribute)

# Examples
## Adding Item Attribute
Note: Attributes can be stacked using this! If you don't want it to stack make sure to remove the attribute before adding a new one.
```
addItemAttribute(item: item, attribute: string, amount: number, operation: integer, slot: string) :: item

set player's tool to addItemAttribute((player's tool), "generic.attack_damage", 4, 1, "mainhand")
```
![image](https://user-images.githubusercontent.com/67760502/221243532-2a9c4bab-a4ef-44e7-9c27-a41580b4437d.png)

## Removing Item Attribute
```
removeItemAttribute(item: item, attribute: string) :: item

set player's tool to removeItemAttribute((player's tool), "generic.attack_damage")
```

## Getting Item Attribute
Note: This can return nothing if the attribute isn't set.
```
getItemAttribute(item: item, attribute: string) :: object

broadcast getItemAttribute((player's tool), "generic.attack_damage")
```

## Checking If Attribute is Set
```
if getItemAttribute((player's tool), "generic.attack_damage") is set:
  broadcast "is set :)" 
```
