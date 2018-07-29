# Your First Plugin

Create a folder inside of your plugins folder. You can name this folder whatever you like as long as it has the `.lkt` extension. For example, `MyFirstLukkitPlugin.lkt` would be a great name to start with. Inside of the folder you have just created, create two more new files named `main.lua` and `plugin.yml`. These files will be used to control and configure your Lukkit plugin.

### Plugin Configuration

The `plugin.yml` file is where information on your plugin, such as the description, author and version will be stored. The format of this file follows the same structure as that of the Bukkit or Spigot `plugin.yml`. However, unlike the `plugin.yml` in Bukkit and Spigot, you are not required to fill out the commands section. More information on the `plugin.yml` file can be found [here](https://bukkit.gamepedia.com/Plugin_YAML), do not include the `commands` section as it will cause errors.

An example of a `plugin.yml` file looks like:

{% code-tabs %}
{% code-tabs-item title="plugin.yml" %}
```yaml
main: main.lua
version: 1.0
name: My-First-Lukkit-Plugin
description: My very first Lukkit plugin.
author: YourName
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Main Lua File

The main Lua file is defined in your `plugin.yml` file and is the first file that is run when your plugin starts. This file does not have to be called name, as long as the name defined in your `plugin.yml` file matches that of your main file.

An example of a main Lua file with the `onEnable` and `onDisable` events looks like:

{% code-tabs %}
{% code-tabs-item title="main.lua" %}
```lua
plugin.onEnable(function()
  logger.info("My first plugin is enabled!")
end)

plugin.onDisable(function()
  logger.info("My first plugin is disabled!")
end)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Commands

Creating commands in Lukkit is simple and requires only three lines of code. When creating a command in Lukkit, information about the command is stored in objects, such as the name and description. More information about commands can be found [here](https://lukkit.net/Commands).

An example of a main Lua file with a command looks like:

{% code-tabs %}
{% code-tabs-item title="main.lua" %}
```lua
plugin.onEnable(function()
  logger.info("My first plugin is enabled!")
end)

plugin.onDisable(function()
  logger.info("My first plugin is disabled!")
end)

local testCommand = plugin.addCommand({name="hello",description="Hello world"}, function(cmd)
    plugin.getServer():broadcastMessage("Hello, world!")
end)

```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Events

Just like creating commands, listening for events in Lukkit is very simple and only requires three lines of code. With events and commands, you can also get information about the player or other information that is returned in the event. More information about events can be found [here](https://lukkit.net/Events).

An example of a main Lua file with an event looks like:

{% code-tabs %}
{% code-tabs-item title="main.lua" %}
```lua
plugin.onEnable(function()
  logger.info("My first plugin is enabled!")
end)

plugin.onDisable(function()
  logger.info("My first plugin is disabled!")
end)

local testCommand = plugin.addCommand({name="hello",description="Hello world"}, function(cmd)
    plugin.getServer():broadcastMessage("Hello, world!")
end)

plugin.registerEvent("BlockBreakEvent", function(event)
    event:getPlayer():sendMessage("You broke a block")
end)
```
{% endcode-tabs-item %}
{% endcode-tabs %}



