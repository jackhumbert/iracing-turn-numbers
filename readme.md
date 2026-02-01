# iRacing Turn Numbers

To be used with [iRon](https://github.com/jackhumbert/iron) or [SimHub](https://github.com/jackhumbert/simhub-jackdash).

JSON files should be in the root directory, and filenames should follow the [iRacing Track Paths](https://support.iracing.com/support/solutions/articles/31000176962-filepath-for-active-iracing-tracks) with the inter-directory `\` replaced with a space (` `). This matches the [WeekendInfo.TrackName](https://sajax.github.io/irsdkdocs/yaml/weekendinfo.html#trackname) variable from the iRacing SDK.

The current format of the JSON file is:

```json
{
  "turns": [
    {
      "name":  "Turn 1",
      "start": 558,
      "end": 1902
    },
    ...
}
```

Where:
  * `name` is the turn name with "Turn" prefixed (some turns have special names)
  * `start` & `end` are the start and end points of the turn (entrance to exit), in meters. This will match [LapDist](https://sajax.github.io/irsdkdocs/telemetry/lapdist.html#lapdist) in the iRacing SDK.
