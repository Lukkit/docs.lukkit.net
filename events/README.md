# Events

Lukkit allows you to hook into events, such as those when a block has been placed or a player has sent a chat message. To register an event, you can use the [`plugin.registerEvent(event: string, callback: function)`](https://docs.lukkit.net/globals/global-variables/plugin) method. The event parameter can be an event listed in the [event list](https://docs.lukkit.net/events/event-list) or a path to a class, such as `org.bukkit.player.PlayerJoinEvent`.
