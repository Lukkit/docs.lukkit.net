# Commands

Lukkit allows you to create simple or even complex commands using just a few simple lines of Lua. Commands created using Lukkit work just the same as a command creating via the Spigot API in Java would. Specifying a name for each command is required, but the other options allow you to extend the command and are optional.

Commands can be created using the [`plugin.addCommand()`](https://docs.lukkit.net/globals/global-variables/plugin) method. Two parameters are required for this method, the first being a [command options](https://docs.lukkit.net/commands/command-options) table and the second a callback function with a single parameter known as the [CommandEvent](https://docs.lukkit.net/commands/command-event).
