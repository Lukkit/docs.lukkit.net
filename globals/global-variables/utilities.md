# Utilities

Represented by `util`.

* **`util.getTableFromList(list: java.util.Collection | java.util.stream.Stream)` : table**

  Convert from a stream or collection in Java to a table in Lua.

* **`util.getTableFromArray(array: array)` : table**

  Convert from a array in Java to a table in Lua.

* **`util.getTableFromMap(map: java.util.Map)` : table**

  Convert from a map in Java to a table in Lua.

* **`util.getTableLength(table: table)` : int**

  Returns the amount of keys available in a table.

* **`util.runAsync(func: function, delay: int)`**

  Run an asynchronous function after a certain time in milliseconds.

* **`util.runDelayed(func: function, delay: int)`**

  Run a synchronous function after a certain time in milliseconds.

* **`util.getClass(class: string)` : java.lang.Class**

  Grab a class from Java using the package and name. \(ie `java.io.File`\)

* **`util.getSkullMeta(item: org.bukkit.inventory.ItemStack)` :** [**SkullWrapper**](https://github.com/artex-development/docs.lukkit.net/tree/9cfd55fd81df8d045428f2ce1c6a2bcf7bc208eb/globals/global-variables/Wrappers/README.md#Skull)\*\*\*\*

  Returns the SkullMeta from an ItemStack.

* **`util.getBannerMeta(item: org.bukkit.inventory.ItemStack)` :** [**BannerWrapper**](https://github.com/artex-development/docs.lukkit.net/tree/9cfd55fd81df8d045428f2ce1c6a2bcf7bc208eb/globals/global-variables/Wrappers/README.md#Banner)\*\*\*\*

  Returns the BennerMeta from an ItemStack.

* **`util.parseItemStack(item: org.bukkit.inventory.ItemStack)` :** [**ItemStackWrapper**](https://github.com/artex-development/docs.lukkit.net/tree/9cfd55fd81df8d045428f2ce1c6a2bcf7bc208eb/globals/global-variables/Wrappers/README.md#ItemStack)\*\*\*\*

  Convert the userdata from an ItemStack into a table.

