[![GitHub Release][releases-shield]][releases]
[![GitHub Activity][commits-shield]][commits]
[![License][license-shield]](LICENSE)
[![hacs][hacsbadge]][hacs]


This custom component for Home Assistant is an upgrade of [awesome_thermostat](https://github.com/dadge/awesome_thermostat) with addition of some usefull features.

## Why another thermostat implementation ?
For my personnal usage, I needed to add a couple of features
This new component is an [awesome_thermostat](https://github.com/dadge/awesome_thermostat) with these additions:
- A delay can be added before turning on/off a thermostat when a window is opened/closed
- Add a `target_temp_step` option like in a [Generic Thermostat](https://www.home-assistant.io/integrations/generic_thermostat) as the awesome_thermostat doesn't seem to handle it

### HACS installation

1. Install [HACS](https://hacs.xyz/). That way you get updates automatically.
2. Add this Github repository as custom repository in HACS settings.
3. search and install "My Awesome Thermostat" in HACS and click `install`.
4. Modify your `configuration.yaml` as explain below.
5. Restart Home Assistant.

### Manual installation

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
2. If you do not have a `custom_components` directory (folder) there, you need to create it.
3. In the `custom_components` directory (folder) create a new folder called `my_awesome_thermostat`.
4. Download _all_ the files from the `custom_components/my_awesome_thermostat/` directory (folder) in this repository.
5. Place the files you downloaded in the new directory (folder) you created.
6. Modify your `configuration.yaml` as explain below
7. Restart Home Assistant

## Minimum requirements

* This implementstion can override or superseed the core generic thermostat

## Configuration

In the following examples we are assuming that you know how to configure an awesome_thermostat (if not please have a look at : https://github.com/dadge/awesome_thermostat ) and we will just highlight the differences in the configuration to apply.

### Window detection delay

Add the following config to turn off a thermostat after a delay after a window/door opening detection (and turn it on again after a closing detection):

```yaml
window_delay: integer
```

This delay is supposed to be expressed in seconds.

### Target temperature step

With an awesome thermostat, the configurable temperature precision is the same as the current temperature precision (configurable with the config `precision`).
We add an extra config to detach the configurable temperature precision from the other one, so one can for example see the exact temperature with a 0.1 precision, but configure the target temperature with a precision of 0.5.

```yaml
target_temp_step: float
```


[awesome_thermostat]: https://github.com/dadge/awesome_thermostat
[commits-shield]: https://img.shields.io/github/commit-activity/y/dadge/awesome_thermostat.svg?style=for-the-badge
[commits]: https://github.com/dadge/awesome_thermostat/commits/master
[hacs]: https://github.com/custom-components/hacs
[hacsbadge]: https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg?style=for-the-badge
[forum]: https://community.home-assistant.io/
[license-shield]: https://img.shields.io/github/license/dadge/simple_thermostat.svg?style=for-the-badge
[maintenance-shield]: https://img.shields.io/badge/maintainer-Joakim%20Sørensen%20%40ludeeus-blue.svg?style=for-the-badge
[releases-shield]: https://img.shields.io/github/release/dadge/awesome_thermostat.svg?style=for-the-badge
[releases]: https://github.com/dadge/awesome_thermostat/releases
