# Discord Webhooks \(http\)



This cool little plugin sends a POST request to a Discord webhook and allow users to send a message to a channel. Some things that could be added or changed would be to send all chat messages to discord, prevent users from using `@everyone` or mentioning users, and running it async so it doesn't slow down the server.

## Code

{% code-tabs %}
{% code-tabs-item title="main.lua" %}
```lua
-- Imports
unirest = import("com.mashape.unirest.http.Unirest")
color = newInstance("#.wrappers.ChatColorWrapper", {plugin.getPlugin()})

webhookUrl = "https://discordapp.com/api/webhooks/532360268223741952/1XLKZg9o3a93AMui2BauKUY7SPTWYe2ec_D9gf2UFEvuJ09L8OHJcSXf4j6HoD7j1Cq5"

local discordCommand = plugin.addCommand({name="discord", permission="lukkit.command.discord"}, function(cmd)
    -- Convert arguments into a single string
    argString = ''
    for i, arg in ipairs(cmd:getArgs()) do
        argString = argString .. arg
    end

    -- Make POST request
    response = unirest:post(webhookUrl):field("username", cmd:getSender():getName()):field("content", argString):asString()

    -- Tell user
    cmd.getSender():sendMessage(color.GREEN .. 'Message sent!')
end)

```
{% endcode-tabs-item %}
{% endcode-tabs %}

