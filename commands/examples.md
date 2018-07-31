# Examples

The following are basic usage examples for commands, the command options and the CommandEvent. Please note that, in each of these examples, the value returned from [`commandEvent.getSender()`](https://docs.lukkit.net/commands/commandevent) is always a player.

### Command Options
This example contains a command in which all command option specifications have been filled.
```lua
plugin.addCommand({name="command", description="Execute the command /command", usage="/command", permission="commands.command", permissionMessage="You cannot execute /command", maxArgs=0, minArgs=0, runAsync=false}, function(commandEvent)
    commandEvent.getSender():sendMessage("You executed /" .. commandEvent.getCommand());
end)
```

### Arguments
This example contains a command that requires arguments to be specified from the player. The list of arguments is returned when calling [`commandEvent.getArgs()`](https://docs.lukkit.net/commands/commandevent) and thus we can use `[1]` to get the first argument that was specified.
```lua
plugin.addCommand({name="command", description="Execute the command /command", usage="/command <message>", minArgs=1}, function(commandEvent)
    commandEvent.getSender():sendMessage("You executed /" .. commandEvent.getCommand() .. " with the message: " .. commandEvent.getArgs()[1])
end)
```
