# Hello, world!

This plugin is very simple. When the plugin loads "Hello, world" is printed to the console. This is a example is great to use as a template.

## Code
### plugin.yml
```yaml
name: Hello-World
author: AL_1
version: "1.0"
description: Just here to say hello
main: main.lua
```

### main.lua
```lua
plugin.onEnable(function()
  logger.info("Hello, world!")
end)

plugin.onDisable(function()
  logger.info("Goodbye, world!")
end)
```
