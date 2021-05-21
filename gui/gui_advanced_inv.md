# GUI

## Create an item with more information

```lua
-- Import utils
local itemStack = import("org.bukkit.inventory.ItemStack")
local javaArrayList = import("java.util.ArrayList")
local material = import("$.Material")
-- Create inventory
local title = "This is the inventory title"
local slots = 9
local inv = bukkit:createInventory(nil, slots, title)

-- Create new item stack
local countOfItems = 1
local newItemStack = luajava.new(itemStack, material.GRASS, countOfItems, 0)
-- Get item meta from new item stack
local meta = newItemStack:getItemMeta()
-- Set new item text
meta:setDisplayName("WoW crazy item")

-- Set new lore to item
local description = {"WoW this is a cool", "description O.o"}
local list = luajava.new(javaArrayList)
for i = 1, #description do
  list:add(description[i])
end
meta:setLore(list)

-- Set the new item meta
newItemStack:setItemMeta(meta)
-- Set item to a slot
local setSlot = 0
inv:setItem(setSlot, newItemStack)
-- Open inventory for player
player:openInventory(inv)
```

This code allows you to set the item name and the lore text
