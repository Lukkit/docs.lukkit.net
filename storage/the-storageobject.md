# The StorageObject

This is the object returned when calling [plugin.getStorageObject\(file: string\)](https://github.com/artex-development/docs.lukkit.net/tree/872d59d6ba1d99b239c03950ebfcb8df546f66aa/storage/Globals/README.md#plugingetstorageobjectfile-string). Here it is represented as `storage`.

## `storage:getType()`: `"yaml"` or `"json"`

Returns the type of the storage object, it will be either `"yaml"` or `"json"`.

## `storage:exists(path: string)`: boolean

Returns true if the path exists in the storage file and false if not

## `storage:setDefaultValue()`: boolean

Sets the default value for a path. Returns true if the value is set and false if not

## `storage:setValue(path: string, value: any)`: boolean

Sets the value of the path in the storage file. Returns false if there was an error setting the value.

## `storage:getValue(path: string)`: any

Gets the value from the storage file from its path.

## `storage:clearValue(path: string)`: boolean

Deletes the value from the storage file from its path. Returns false if there was an error setting the value.

## `storage:save()`

Save the current storage object to its file. It is recommended to do this on plugin disable.

