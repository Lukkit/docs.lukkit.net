# Server

Events related to programmatic state changes via the server.

| Event| Description |
| --- | --- |
| BroadcastMessageEvent | Event triggered for server broadcast messages such as from `plugin.getServer():broadcast(String, String)`. |
| MapInitializeEvent | Called when a map is initialized. |
| PluginDisableEvent | Called when a plugin is disabled. |
| PluginEnableEvent | Called when a plugin is enabled. |
| PluginEvent | Used for plugin enable and disable events |
| RemoteServerCommandEvent | This event is called when a command is received over RCON. |
| ServerCommandEvent | This event is called when a command is run by a non-player. |
| ServerEvent | Miscellaneous server events |
| ServerListPingEvent | Called when a server list ping is coming in. |
| ServiceEvent | An event relating to a registered service. |
| ServiceRegisterEvent | This event is called when a service is registered. |
| ServiceUnregisterEvent | This event is called when a service is unregistered. |
| TabCompleteEvent | Called when a CommandSender of any description (ie: player or console) attempts to tab complete. |
