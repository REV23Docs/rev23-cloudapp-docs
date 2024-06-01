# Cache

On iPad we cache some data to prevent constant round trips to the cloud for things that don't change often. Things like Medical Conditions, Sources, Service Types, Jewelry Types, etc... are cached on the device for about 24 hours. Once the cache expires, we retrieve a fresh copy of the data.

> When a Kiosk session begins any critical data used for forms is refreshed immediately to make sure you always have the latest version.

Because we cache some of this data you may notice some inconsistencies in some scenarios, for instance, if you create/update or delete data on another device or web app, you may not see those changes on your device right away.

If you only use one device, you really don't have to worry about the cache all that much because the caches update as you use them. For example, if you add a new source, the source cache is automatically up to date.

However, if you see any inconsistencies there are two easy ways to fix/update the cache.

- **Method 1:** Go to Cache from the menu and delete all cache entries, or just the one you need to refresh.

- **Method 2:** From most screens in Settings you can use the pull down/hold/release gesture to refresh the cache and show the updated data.
