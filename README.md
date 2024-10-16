# Interfaces Refresher

Requirements
------------

```
# opkg update && opkg install at jq screen
```


Installation
------------

1. Clone this repo to `/root/interfaces-refresher`

```
# git clone https://github.com/aztecrabbit/interfaces-refresher /root/interfaces-refresher
```

2. Save this code to `Scheduled Tasks` a.k.a `crontab`

`Menu > System > Scheduled Tasks`

```
*/1 * * * * /root/interfaces-refresher/interfaces-watcher
```

That code will execute `/root/interfaces-refresher/interfaces-watcher` every minute. `Recommended`.

3. Change openclash dashboard secret to `darktunnel`

`Menu > Services > OpenClash > Plugin Settings > Dashboard Settings > Dashboard Secret` then `Apply Settings`

This step is important, all download connection, stream connection, etc. can be resumed automaticly, no need to manually refresh stream or download link again.


Notes
-----

- Tested on `Dell Inc. DW5821e Snapdragon X20 LTE`, downtime `< 2 seconds`.
- You can manually refresh interface if the internet not responding correctly, just execute this command,

```
# /root/interfaces-refresher/interfaces-refresher
```
