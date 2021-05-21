# GUI

## Run a function if an inventory item has been clicked

```lua
plugin.registerEvent("InventoryClickEvent", function(e)
  -- Get info
  local player = e:getWhoClicked()
  local inventoryName = e:getView():getTitle()
  
  -- Test if the clicked slot is not empty
  if e:getCurrentItem() then
     if e:getCurrentItem():getItemMeta() then
        if e:getCurrentItem():getItemMeta():getDisplayName() then
           -- Get item text
           local clickedItemName = e:getCurrentItem():getItemMeta():getDisplayName()
           -- Test if open inv has contains the name
           if string.find(inventoryName, "This is the inventory title") then
              if string.find(clickedItemName, "WoW crazy item") then
                  -- Here comes your code if the generated item with this name is clicked
              end
              -- Disable dragging or dropping item to this inv
              e:setCancelled(true)
           end
        end
     end
  end
end)
```

You need to register the event *InventoryClickEvent* with [`plugin.registerEvent(event: string, callback: function)`](https://docs.lukkit.net/globals/global-variables/plugin) to test the clicked item in inventory
