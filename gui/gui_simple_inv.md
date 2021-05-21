# GUI

## Create a simple inventar

```lua
local title = "This is the inventory title"
local slots = 9
local inv = bukkit:createInventory(nil, slots, title)
player:openInventory(inv)
```
**Make sure thah your slots number can be divided by 9 and is lower then 55 (max. Slots 54)**

## Set an item for the inventory

```lua
local itemStack = import("org.bukkit.inventory.ItemStack")
local material = import("$.Material")
local title = "This is the inventory title"
local slots = 9
local inv = bukkit:createInventory(nil, slots, title)

local countOfItems = 1
local newItemStack = luajava.new(itemStack, material.GRASS, countOfItems, 0)
local setSlot = 0
inv:setItem(setSlot, newItemStack)

player:openInventory(inv)
```

This code allows you to open an inventory with an grass block item in the first slot of the inventory
