# Cache

On iPad we cache (save copies of) some data to prevent constant round trips to the cloud for things that don't change often. Data such as Medical Conditions, Sources, Service Types, Jewelry Types, etc... are cached on each device typically for 24 hours. Once the cache expires, we retrieve a fresh copy of the data.

> When a Kiosk session begins, any critical data required for this purpose is refreshed immediately to make sure you always have the latest version.

Because we cache some of this data you may notice some inconsistencies in some scenarios, for instance, if you create/update or delete data on another device or web app, you may not see those changes on another device right away.

If you only use one device, you really don't need to worry about the cache all that much because the caches update as you use them. For example, if you add a new source on the iPad, the source cache is automatically up to date.

However, if you see any inconsistencies there are two easy ways to fix/update the cache.

- **Method 1:** Tap the main menu on the top left, go to Support then tap Cache. Delete all cache entries, or just the one you need to refresh.

- **Method 2:** From most screens in Settings you can use the pull down/hold/release gesture to refresh the cache and show the updated data.
