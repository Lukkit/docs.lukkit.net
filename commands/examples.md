# Examples

The following are basic examples of commands, command options and the CommandEvent and how each can be used. Please note that, in each of these examples, the value returned from [commandEvent.getSender()](#commandeventgetsender-orgbukkitcommandcommandsender) is a player.

### Command Options
This example contains a command with all command options specified.
```lua
plugin.addCommand({name="command", description="Execute the command /command", usage="/command", permission="commands.command", permissionMessage="You cannot execute /command", maxArgs=0, minArgs=0, runAsync=false}, function(commandEvent)
    commandEvent.getSender():sendMessage("You executed /" .. commandEvent.getCommand());
end)
```

### Arguments
This example contains a command that requires arguments. The list of arguments is returned when calling [commandEvent.getArgs()](#commandeventgetargs-array) and thus we can use `[1]` to grab the first argument that was specified.
```lua
plugin.addCommand({name="command", description="Execute the command /command", usage="/command <message>", minArgs=1}, function(commandEvent)
    commandEvent.getSender():sendMessage("You executed /" .. commandEvent.getCommand() .. " with the message: " .. commandEvent.getArgs()[1])
end)
```
