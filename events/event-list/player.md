# Player

Events for players.

| Event | Description |
| :--- | :--- |
| AsyncPlayerChatEvent | This event will sometimes fire synchronously, depending on how it was triggered. |
| AsyncPlayerPreLoginEvent | Stores details for players attempting to log in. |
| PlayerAchievementAwardedEvent    Deprecated | future versions of Minecraft do not have achievements |
| PlayerAdvancementDoneEvent | Called when a player has completed all criteria in an advancement. |
| PlayerAnimationEvent | Represents a player animation event |
| PlayerArmorStandManipulateEvent | Called when a player interacts with an armor stand and will either swap, retrieve or place an item. |
| PlayerBedEnterEvent | This event is fired when the player is almost about to enter the bed. |
| PlayerBedLeaveEvent | This event is fired when the player is leaving a bed. |
| PlayerBucketEmptyEvent | Called when a player empties a bucket |
| PlayerBucketEvent | Called when a player interacts with a Bucket |
| PlayerBucketFillEvent | Called when a player fills a bucket |
| PlayerChangedMainHandEvent | Called when a player changes their main hand in the client settings. |
| PlayerChangedWorldEvent | Called when a player switches to another world. |
| PlayerChannelEvent | This event is called after a player registers or unregisters a new plugin channel. |
| PlayerChatEvent | Deprecated. This event will fire from the main thread and allows the use of all of the Bukkit API, unlike the AsyncPlayerChatEvent. |
| PlayerChatTabCompleteEvent | Called when a player attempts to tab-complete a chat message. |
| PlayerCommandPreprocessEvent | This event is called whenever a player runs a command \(by placing a slash at the start of their message\). |
| PlayerDropItemEvent | Thrown when a player drops an item from their inventory |
| PlayerEditBookEvent | Called when a player edits or signs a book and quill item. |
| PlayerEggThrowEvent | Called when a player throws an egg and it might hatch |
| PlayerEvent | Represents a player related event |
| PlayerExpChangeEvent | Called when a players experience changes naturally |
| PlayerFishEvent | Thrown when a player is fishing |
| PlayerGameModeChangeEvent | Called when the GameMode of the player is changed. |
| PlayerInteractAtEntityEvent | Represents an event that is called when a player right clicks an entity that also contains the location where the entity was clicked. |
| PlayerInteractEntityEvent | Represents an event that is called when a player right clicks an entity. |
| PlayerInteractEvent | Represents an event that is called when a player interacts with an object or air, potentially fired once for each hand. |
| PlayerItemBreakEvent | Fired when a player's item breaks \(such as a shovel or flint and steel\). |
| PlayerItemConsumeEvent | This event will fire when a player is finishing consuming an item \(food, potion, milk bucket\). |
| PlayerItemHeldEvent | Fired when a player changes their currently held item |
| PlayerItemMendEvent | Represents when a player has an item repaired via the Mending enchantment. |
| PlayerJoinEvent | Called when a player joins a server |
| PlayerKickEvent | Called when a player gets kicked from the server |
| PlayerLevelChangeEvent | Called when a players level changes |
| PlayerLocaleChangeEvent | Called when a player changes their locale in the client settings. |
| PlayerLoginEvent | Stores details for players attempting to log in |
| PlayerMoveEvent | Holds information for player movement events |
| PlayerPickupArrowEvent | Thrown when a player picks up an arrow from the ground. |
| PlayerPickupItemEvent | Deprecated. Use EntityPickupItemEvent |
| PlayerPortalEvent | Called when a player is about to teleport because it is in contact with a portal. |
| PlayerPreLoginEvent | Deprecated. This event causes synchronization from the login thread; AsyncPlayerPreLoginEvent is preferred to keep the secondary threads asynchronous. |
| PlayerQuitEvent | Called when a player leaves a server |
| PlayerRegisterChannelEvent | This is called immediately after a player registers for a plugin channel. |
| PlayerResourcePackStatusEvent | Called when a player takes action on a resource pack request sent via Player.setResourcePack\(java.lang.String\). |
| PlayerRespawnEvent | Called when a player respawns. |
| PlayerShearEntityEvent | Called when a player shears an entity |
| PlayerStatisticIncrementEvent | Called when a player statistic is incremented. |
| PlayerSwapHandItemsEvent | Called when a player swap items between main hand and off hand using the hotkey. |
| PlayerTeleportEvent | Holds information for player teleport events |
| PlayerToggleFlightEvent | Called when a player toggles their flying state |
| PlayerToggleSneakEvent | Called when a player toggles their sneaking state |
| PlayerToggleSprintEvent | Called when a player toggles their sprinting state |
| PlayerUnleashEntityEvent | Called prior to an entity being unleashed due to a player's action. |
| PlayerUnregisterChannelEvent | This is called immediately after a player unregisters for a plugin channel. |
| PlayerVelocityEvent | Called when the velocity of a player changes. |

