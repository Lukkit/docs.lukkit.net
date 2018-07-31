# Examples

This method hooks to the BlockBreakEvent event and messages the player that they just broke a block.
```lua
plugin.registerEvent("BlockBreakEvent", function(e)
    e:getPlayer():sendMessage("You broke a break")
end)
```

This next code block is a full plugin example that when the player does the command `/inspect` it puts them into a table then when they break a block it cancels the event and tells the player what block they broke. They can then run the same command again to no longer receive what block they broke.
```lua
-- Imports
material = import("$.Material")
color = newInstance("#.wrappers.ChatColorWrapper", {plugin.getPlugin()})

-- An inspect command with an event to tell what a block is
inspecters = {}

-- Add the command
local inspectCommand = plugin.addCommand({name="inspect"}, function(cmd)
    local sender = cmd.getSender()
    -- Make sure it's a player sending the command
    if not cmd.isPlayerSender() then
        sender:sendMessage(color.DARK_RED:toString() .. "Only players can run this command!")
        return
    end
    -- Go through every inspector and check if any equals this players uuid
    for k,v in pairs(inspecters) do
      if v == sender:getUniqueId() then
            -- Remove them from inspectors and tell them
            table.remove(inspecters, k)
            sender:sendMessage(color.YELLOW .. "You are no longer an inspector")
            return
        end
    end
    -- Else, add them and tell them
    table.insert(inspecters, sender:getUniqueId())
    sender:sendMessage(color.YELLOW .. "You are now an inspector")
end)

-- Add the event
plugin.registerEvent("BlockBreakEvent", function(e)
    -- Go through every inspector and check if any equals this players uuid
    for _,v in pairs(inspecters) do
      if v == e:getPlayer():getUniqueId() then
            -- Tell them the block
            e:getPlayer():sendMessage(color.AQUA .. "That is " .. color.GOLD .. e:getBlock():getType():name())
            e:setCancelled(true)
            break
      end
    end
end)
```
