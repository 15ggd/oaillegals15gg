
# Oaexploits Plugin

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
```

### Command Whitelist and Blacklist
Configure the command whitelist and blacklist in the `config.yml` file:
```yaml
command-whitelist:
  enabled: false
  commands:
    - "help"
    - "list"

command-blacklist:
  enabled: true
  commands:
    - "plugins"
    - "op"
```

### Debug Mode
Enable or disable debug mode in the `config.yml` file:
```yaml
debug-mode: true
```

### Illegal Items and Overleveled Enchantments
Configure the removal options in the `config.yml` file:
```yaml
removal-options:
  remove-illegal-items: true
  remove-overleveled-enchantments: true
```

### Additional Configurations
Configure additional settings in the `config.yml` file:
```yaml
illegal-items:
  blocks:
    - "BEDROCK"
    - "COMMAND_BLOCK"
  items:
    - "ENDER_PEARL"
    - "ELYTRA"

additional-configs:
  inventory-scan-depth: 3

admin-alerts:
  enabled: true
  cooldown: 60
```

## Development

### Prerequisites
- Java Development Kit (JDK)
- Maven

### Building the Plugin
1. Clone the repository.
2. Navigate to the project directory.
3. Run `mvn clean package` to build the plugin jar file.

### Contributing
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Push to your branch.
5. Create a pull request.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contact
For any questions or support, please open an issue in the GitHub repository.
