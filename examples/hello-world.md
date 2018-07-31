# Hello, world!

This is a simple plugin that will print two messages to the server console, one when the plugin has been enabled and one when the plugin has been disabled.

### Code
{% code-tabs %} {% code-tabs-item title="plugin.yml" %}
```yaml
name: hello-world
author: AL_1
version: "1.0"
description: "Hello, world!"
main: main.lua
```
{% endcode-tabs-item %} {% endcode-tabs %}

{% code-tabs %} {% code-tabs-item title="main.lua" %}
```lua
plugin.onEnable(function()
  logger.info("Hello, world!")
end)

plugin.onDisable(function()
  logger.info("Goodbye, world!")
end)
```
{% endcode-tabs-item %} {% endcode-tabs %}
