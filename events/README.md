# Events

Lukkit allows you to hook into the events of Bukkit such as when a block is broken or a player sends a chat message. To register a event you must use the [plugin.registerEvent(event: string, callback: function)](Globals#pluginregistereventevent-string-callback-function) method. The event parameter can be one of the events listed in the [event list](#event-list) or a classpath such as `org.bukkit.player.PlayerJoinEvent`
