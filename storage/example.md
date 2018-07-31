# Example

In this example, a storage object is created for the `config.yml` file and sets the default value `join-message`. Then when the [player event](Events#player) `PlayerJoinEvent` is called it gets the storage value from the [storage object](#storageobject), replaces `%s` with the player name and sets it to the join message.
```lua
-- Create a storage object with the file "config.yml"
pluginConfig = plugin.getStorageObject("config.yml")

-- Set the default to join message and save the config if it is not already in there
if pluginConfig:setDefaultValue("join-message", "%s joined the game!") then
    pluginConfig:save()
end

-- Make event for when players join
plugin.registerEvent("PlayerJoinEvent", function(event)
    -- Set the join message based on the config value
    event:setJoinMessage(string.format(pluginConfig:getValue("join-message"), event:getPlayer():getDisplayName()))
end)
```
