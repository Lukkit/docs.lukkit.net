# Command Event

The command event is passed through the callback function of the [plugin.addCommand\(\)](../globals/global-variables/plugin.md) method. This event has certain properties that can help you when creating the function of your command. This even is known as `commandEvent` in the [examples](examples.md). Look there to see how it is used.

* **`commandEvent.isPlayerSender()`: boolean** Returns true if the sender of the command is a player or false otherwise.
* **`commandEvent.isConsoleSender()`: boolean** Returns true if the sender of the command is the console or false otherwise.
* **`commandEvent.isBlockSender()`: boolean** Returns true if the sender of the command is a block \(e.g. command block\) or false otherwise.
* **`commandEvent.isEntitySender()`: boolean** Returns true if the sender of the command is an entity \(can be a player\) or false otherwise.
* **`commandEvent.getSender()`:** [**org.bukkit.command.CommandSender**](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/command/CommandSender.html) ****Returns the sender of the command.
* **`commandEvent.getArgs()`: array** Returns the arguments of the command.
* **`commandEvent.getCommand()`: string** Returns the name of the command.

