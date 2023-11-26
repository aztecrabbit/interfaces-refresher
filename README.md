# Interfaces Refresher

Requirements
------------

```
# opkg update && opkg install at jq
```


Installation
------------

1. Save `interfaces-watcher` and `interfaces-refresher` to `/root/`

```
/root/interfaces-refresher
/root/interfaces-watcher
```

Run chmod to be able to execute that files.

```
# chmod +x /root/interfaces-refresher /root/interfaces-watcher
```

2. Save this code to `Scheduled Tasks` a.k.a `crontab`

`Menu > System > Scheduled Tasks`

```
*/1 * * * * /root/interfaces-watcher
```

That code will execute `/root/interfaces-watcher` every minute. `Recommended`.


Notes
-----

Tested on `Dell Inc. DW5821e Snapdragon X20 LTE`, downtime `< 2 seconds`.
