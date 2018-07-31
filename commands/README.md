# Commands

Lukkit allows you to create simple, or even complex, commands using just a few simple lines. Commands created using Lukkit work just as a command would had it been registered through the Spigot API via a plugin created using Java. Specifying a name for each command is required, but the other options allow you to extend the command and are optional.

Commands can be created using the [plugin.addCommand()](Globals#addcommand) method. Two parameters are required for this method, the first being a [command options](#command-options) table and the second a callback function with a single parameter known as the [CommandEvent](#commandevent).
