# GUI

## Create a simple inventar

```lua
-- Create inventory
local title = "This is the inventory title"
local slots = 9
local inv = plugin.getServer():createInventory(nil, slots, title)
-- Open inventory for player
player:openInventory(inv)
```
**Make sure thah your slots number can be divided by 9 and is lower then 55 (max. Slots 54)**

## Set an item for the inventory

```lua
-- Import utils
local itemStack = import("org.bukkit.inventory.ItemStack")
local material = import("$.Material")
-- Create inventory
local title = "This is the inventory title"
local slots = 9
local inv = plugin.getServer():createInventory(nil, slots, title)

-- Create new item stack
local countOfItems = 1
local newItemStack = luajava.new(itemStack, material.GRASS, countOfItems, 0)
-- Set item to a slot
local setSlot = 0
inv:setItem(setSlot, newItemStack)
-- Open inventory for player
player:openInventory(inv)
```

This code allows you to open an inventory with an grass block item in the first slot of the inventory
