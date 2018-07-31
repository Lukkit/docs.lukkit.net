# Toggle Fly

This plugin allows users with the permission node `lukkit.command.fly` to begin flying when the player runs the `/fly` command. This plugin makes use of importing the chat color wrapper in order for colors to be used in messages. 

Comments have been added to this plugin for your benefit.

### Code
{% code-tabs %} {% code-tabs-item title="plugin.yml" %}
```yaml
name: Fly-Plugin
author: AL_1
version: "1.3"
description: A plugin to let players fly!
main: main.lua
```
{% endcode-tabs-item %} {% endcode-tabs %}

{% code-tabs %} {% code-tabs-item title="main.lua" %}
```lua
-- Imports
color = newInstance("#.wrappers.ChatColorWrapper", {plugin.getPlugin()})

-- A simple fly command
local flyCommand = plugin.addCommand({name="fly", permission="lukkit.command.fly"}, function(cmd)
    local sender = cmd.getSender()
    -- Make sure it's a player sending the command
    if not cmd.isPlayerSender() then
        sender:sendMessage(color.DARK_RED .. "Only players can fly, silly!")
        return
    end
    
    -- If the player is flying the make them fly, otherwise make them fall
    if sender:isFlying() then
        sender:setFlying(false)
        sender:setAllowFlight(false)
        sender:sendMessage(color.RED .. "Fly off")
    else
        -- This allows the player to fly
        sender:setAllowFlight(true)
        sender:setFlying(true)
        -- The player won't fly if it is on the ground, so we need to move them up a little
        sender:teleport(sender:getLocation():add(0, 0.000001, 0))
        sender:sendMessage(color.GREEN .. "Fly on")
    end
end)
```
{% endcode-tabs-item %} {% endcode-tabs %}
