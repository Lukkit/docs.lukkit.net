# CommandEvent

The CommandEvent is passed through the callback function for the second parameter of the [`plugin.addCommand()`](https://docs.lukkit.net/globals/global-variables/plugin) method. This event has certain properties that might help you while creating your command, which are all listed below. The CommandEvent is represented as `commandEvent` for the [examples](https://docs.lukkit.net/commands/examples) on the next page.

- ### `commandEvent.isPlayerSender()`: boolean
Returns true if the sender of the command is a player or false otherwise.

- ### `commandEvent.isConsoleSender()`: boolean
Returns true if the sender of the command is the console or false otherwise.

- ### `commandEvent.isBlockSender()`: boolean
Returns true if the sender of the command is a block (e.g. command block) or false otherwise.

- ### `commandEvent.isEntitySender()`: boolean
Returns true if the sender of the command is an entity (can be a player) or false otherwise.

- ### `commandEvent.getSender()`: [org.bukkit.command.CommandSender](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/command/CommandSender.html)
Returns the sender of the command.

- ### `commandEvent.getArgs()`: array
Returns the arguments of the command.

- ### `commandEvent.getCommand()`: string
Returns the name of the command.
