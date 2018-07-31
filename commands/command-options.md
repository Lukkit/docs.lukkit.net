# Command Options

The command options table is the first required parameter of the [plugin.addCommand()](Globals#addcommand) method and the following is a list of specifications that can be made for the command options table.

| Specification | Description
| --- | ---
| name * | Name of the command
| description | Description of the command
| usage | Message displayed when the command has been executed in an incorrect manner
| permission | Permission node required to execute the command
| permissionMessage | Message displayed when the user executing the command does not have the required permission node
| maxArgs | The maximum amount of arguments for the command
| minArgs | The minimum amount of arguments for the command
| runAsync | True or false, whether the function should be run in an asynchronous manner

\* = required

## CommandEvent
The command event is passed through the callback function of the [plugin.addCommand()](Globals#addcommand) method. This event has certain properties that can help you when creating the function of your command. This even is known as `commandEvent` in the [examples](#examples) below. Look there to see how it is used.

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
