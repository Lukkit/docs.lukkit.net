# Command Options

The command options table is the first required parameter for the [`plugin.addCommand()`](https://docs.lukkit.net/globals/global-variables/plugin) method and the following is a list of specifications that can be made using the table.

Remember that name is the one specification that is required for each command.

| Specification | Description |
| :--- | :--- |
| name | Name of the command |
| description | Description of the command |
| usage | Message displayed when the command has been executed in an incorrect manner |
| permission | Permission node required to execute the command |
| permissionMessage | Message displayed when the user executing the command does not have the required permission node |
| maxArgs | The maximum amount of arguments for the command |
| minArgs | The minimum amount of arguments for the command |
| runAsync | True or false, whether the function should be run in an asynchronous manner |

