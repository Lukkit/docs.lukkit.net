# Storage

The storage system that has been implemented into Lukkit allows you to create configuration and storage files for your plugin. Creating a file super simple, all you have to do is call the `plugin.getStorageObject(file: string)` method. The file parameter is relative to the data folder for the plugin and has support for both YAML and JSON files.

