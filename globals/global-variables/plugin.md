# Plugin

Represented by `plugin`.

* **`plugin.onLoad(callback: function)`**

  Event called when the plugin has been loaded.

  ```lua
  plugin.onLoad(function()
  logger.info("Plugin loaded")
  end)
  ```

* **`plugin.onEnable(callback: function)`**

  Event called when the plugin has been enabled.

  ```lua
  plugin.onEnable(function()
  logger.info("Plugin enabled")
  end)
  ```

* **`plugin.onDisable(callback: function)`**

  Event called when the plugin has been disabled.

  ```lua
  plugin.onDisable(function()
  logger.info("Plugin disabled")
  end)
  ```

* **`plugin.addCommand(options: table, callback: function)` :** [**Command**](https://github.com/artex-development/docs.lukkit.net/tree/b600fc95db6df12a29cf3c019492ca125cee8319/globals/global-variables/Commands/README.md#command)\*\*\*\*

  Create a command. More information on creating commands can be found [here](https://github.com/artex-development/docs.lukkit.net/tree/b600fc95db6df12a29cf3c019492ca125cee8319/globals/global-variables/Commands/README.md).

  ```lua
  local testCommand = plugin.addCommand({name="hello",description="Hello world"}, function(cmd)
    plugin.getServer():broadcastMessage("Hello, world!")
  end)
  ```

* **`plugin.registerEvent(event: string, callback: function)`**

  Register an event. More information on registering events can be found [here](https://github.com/artex-development/docs.lukkit.net/tree/b600fc95db6df12a29cf3c019492ca125cee8319/globals/global-variables/Events/README.md).

  ```lua
  plugin.registerEvent("BlockBreakEvent", function(e)
    e:getPlayer():sendMessage("You broke a break")
  end)
  ```

* **`plugin.getServer()` :** [**org.bukkit.Server**](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Server.html)\*\*\*\*

  Returns the server object. This is equivalent to `Bukkit.getServer()` in Java.

  ```lua
  local server = plugin.getServer()
  ```

* **`plugin.isNaggable()` : boolean**

  Returns true if the plugin can nag to the log or false otherwise.

  ```lua
  if plugin.isNaggable() then
    logger.info("Plugin is naggable")
  end
  ```

* **`plugin.setNaggable(nag: boolean)`**

  Set the nagging state.

  ```lua
  plugin.setNaggable(true)
  ```

* **`plugin.exportResource(path: string, replace: boolean)`:**

  Export a resource from inside of the plugin workspace to the plugin's data folder.

* **`plugin.getStorageObject(file: string)` :** [**StorageObject**](https://github.com/artex-development/docs.lukkit.net/tree/b600fc95db6df12a29cf3c019492ca125cee8319/globals/global-variables/Storage/README.md#storageobject)\*\*\*\*

  Read a YAML or JSON storage file. More information and examples on storage files can be found [here](https://github.com/artex-development/docs.lukkit.net/tree/b600fc95db6df12a29cf3c019492ca125cee8319/globals/global-variables/Storage/README.md).

