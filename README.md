# Esp Buddy 

This script allows to easely upload firmwares to remote (ESP8266 based) devices using Wifi (Over The Air) or Serial. 
It also gather various tools command to be used in batch mode.

_This is typically a **WORK IN PROGRESS :-) !!!**_


## Features
 - OTA upload on 4M devices
 - OTA upload on 1M devices using an intermediate firmware (automatic two steps)
 - Use configuration presets for devices
 - Optional compilation using platformio
 - Optionally pass various -D flags to the compiler, including extracted parameters like IP or hostname_
 - Fetch Remote devices versions
 - Ping Remote Host
 - Parse Repositories installed versions
 - Git Pull Repositories
 
## Supported (tested) Firmwares
Works with :
- [**ESPeasy**](https://github.com/letscontrolit/ESPEasy/)
- [**Espura**](https://github.com/xoseperez/espurna)
- should virtually works with any ESP8266 firmware

## Installation
- Rename _config-sample.php_ to _config.php_.
- Fill some hosts and configurations in config.php

## Usage

**espbuddy.php COMMAND [OPTIONS]**

Examples:
- `espbuddy.php help` show help
- `espbuddy.php upload` choose from the list of host the one to upload to
- `espbuddy.php upload led1` upload to host 'led1'
- `espbuddy.php upload all -b` upload to all defined hosts , while building the firmware first 
- `espbuddy.php upload led1 -w` upload using serial to host 'led1'
- `espbuddy.php version all` show versions of all defined hosts
- `espbuddy.php ping all` ping of all defined hosts

