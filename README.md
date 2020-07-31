# My Home Assistant configuration

My [Home Assistant](https://home-assistant.io/) Configuration Files

## Inspiration and Support

- [Instagraeme](https://github.com/Instagraeme/Home-Assistant-Configuration)
- [happyleavesaoc](https://github.com/happyleavesaoc/my-home-automation)
- [skalavala](https://github.com/skalavala/smarthome)

Thanks to all the people in the [Home Assistant Forum](https://community.home-assistant.io/) for listening and help

And thanks to *all* the devs that create the Home Assistant magic


## Devices

- Alexa Devices
- Augus Door Lock
- Bali ZWave Shades
- Broadlink RM Pro
- Broadlink RM Pro +
- Broadlink E-Air Sensor
- Eight Sleep Smart Mattress
- Philips Hue Bridge
- Philips Hue Bloom
- Philips Hue Color Ambiance Bulbs
- Philips Hue LightStrip
- Plex Media Server
- Rachio Smart Sprinkler Controller
- Nest Thermostat
- Nest Protect
- Nortek HUSBZB-1 ZWave, ZigBee Hub
- Sonoff switches, plugs and relays
- Ubiquiti Unifi Controller
- Wemo Switches
- Zanzito Device Tracker
- Xiaomi Mi Robot Vacuum


## Plugins

- button-card.js - https://github.com/custom-cards/button-card
- mini-graph-card-bundle.js - https://github.com/kalkih/mini-graph-card
- slider-entity-row.js - https://github.com/thomasloven/lovelace-slider-entity-row
- vertical-stack-in-card.js - https://github.com/ofekashery/vertical-stack-in-card



## Configuration Best Pratices

### More than one entity

Always use a YAML list when you have multiple entries (Style #1 from the documentation).

Yes:
```yaml
sensor:
- platform: mqtt
- platform: forecastio
```

No:
``` yaml
sensor:
  platform: mqtt

sensor 2:
  platform: forecastio
```

### When to use `!secret`

* Private data.
* Constants.

### Namespaces

Use them. Prevents conflicts once you have many sensors, disambiguates generic names, and lends context when referenced. Some components have hardcoded namespacing - don't double up.

### Automations

* Always provide an override switch, use as a condition.
* Inline scripts as actions, unless the script is used in multiple automations.

### Scripts

* Hide scripts that shouldn't be manually triggered.

### Scenes

* Hide scenes that shouldn't be manually triggered.

### Customizations

The interface should be intuitive to encourage use and reduce the learning curve.

* Always set a relevant icon if available (https://materialdesignicons.com/).
* Always set a friendly, descriptive name if the default is insufficient (vague, awkward, computer-generated, etc).

### Includes

Includes help organize configurations. Do not place all configuration in `configuration.yaml`. Split configuration sections to their own files as they grow. Consider splitting up any section that you cannot view without scrolling your editor.
