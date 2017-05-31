Configuration Best Pratices
More than one entity

Always use a YAML list when you have multiple entries (Style #1 from the documentation).

Yes:

sensor:
- platform: mqtt
- platform: google

No:

sensor:
  platform: mqtt

sensor 2:
  platform: google
