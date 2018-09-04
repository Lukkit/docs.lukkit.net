# Global Functions

Functions for importing Lua modules and creating new instances also allow the use of various placeholders that can cut down on development time and create an organized environment. Pound symbols `#` inserted in parameter strings are replaced with `nz.co.jammehcow.lukkit.environment` and dollar signs `$` with `org.bukkit`.

* **`require_local(path: string)` : script**

  Import Lua modules into the current script. This function is the same as the original Lua require method and can be used in that manner. The specified path must be relative to the location of the current Lua script. In the following example, the file extension `.lua` is not necessary for importing modules.

  ```lua
  utils = require 'utils'
  ```

* **`import(class: string)` : static Java class**

  Import an enum or static class from Java into the current script.

  ```lua
  local material = import("$.Material")
  ```

* **`newInstance(class: string, args: array)` : Java object**

  Create a new instance of an object from Java.

  ```lua
  color = newInstance("#.wrappers.ChatColorWrapper", {plugin.getPlugin()})
  plugin.getServer():broadcastMessage(color.GOLD .. "Hello world!")
  ```

