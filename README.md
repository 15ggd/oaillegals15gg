# Oaexploits Plugin

![Stars](https://img.shields.io/github/stars/fanlimgames/oaexploits?style=social&color=green)
![Downloads](https://img.shields.io/github/downloads/fanlimgames/oaexploits/total?color=green)
![Forks](https://img.shields.io/github/forks/fanlimgames/oaexploits?style=social&color=green)

## support 
https://discord.gg/xyhwEzzVXV
## you can get support on this discord 




Oaexploits is a Minecraft plugin designed to enhance server security by blocking unauthorized commands, removing illegal items, managing deop actions on player leave, and handling various configuration tasks. This plugin aims to provide server administrators with tools to maintain a fair and secure gameplay environment.

## Features

### 1. Command Blocking
- **Whitelist and Blacklist:** Allows server administrators to define specific commands that are either allowed (whitelisted) or blocked (blacklisted).
- **Preprocess Event Handling:** Blocks certain commands (e.g., `/give`, `/i`, `/item`) for non-operators, ensuring only authorized players can use them.

### 2. Deop on Leave
- **Automatic Deop:** Automatically deops players who leave the server unless they are whitelisted.
- **Inventory Clearing:** Clears the inventory of deopped players.
- **Teleportation:** Teleports deopped players to a predefined location.
- **Game Mode Reset:** Resets the game mode of deopped players to survival.
- **Custom Messages:** Sends customizable messages to deopped players informing them of the actions taken.

### 3. Illegal Items Removal
- **Automatic Detection:** Detects and removes illegal items and over-leveled enchantments from players' inventories and various storage entities.
- **Admin Alerts:** Alerts administrators when illegal items are detected and removed.
- **Configurable Depth:** Scans nested inventories such as shulker boxes to a configurable depth.

### 4. Chunk Management
- **Chunk Scanning:** Scans chunks for illegal items and removes them.
- **Entity Handling:** Checks entities like storage minecarts and chested animals for illegal items.

## Getting Started

### Installation
1. Download the plugin jar file and place it in the `plugins` folder of your Minecraft server.
2. Start the server to generate the default configuration files.
3. Configure the plugin as needed by editing the `config.yml` and `worldstats.yml` files in the `plugins/Oaexploits` folder.

### Configuration
- `config.yml`: Main configuration file for the plugin.
- `worldstats.yml`: Configuration file for managing world statistics.

### Commands
- `/oaexploits`: Reloads the plugin configuration.
- `/worldstats`: Displays world statistics.

## Usage

### Deop on Leave Configuration
To enable or disable the deop on leave feature and customize its behavior, modify the `config.yml` file:
```yaml
deop-on-leave:
  enabled: true
  whitelist:
    players:
      - "admin"
  teleport:
    world: "world"
    x: 0.0
    y: 64.0
    z: 0.0
    yaw: 0.0
    pitch: 0.0
  message: "&cYou have been deopped, your inventory cleared, and you have been teleported to the spawn point."
