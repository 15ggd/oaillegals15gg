
## support 
https://discord.gg/xyhwEzzVXV
## you can get support on this discord 



### OaExploits Plugin

Welcome to the OaExploits plugin! This powerful and versatile plugin is designed to help manage and maintain order on anarchy servers and other Minecraft servers that face issues with illegal items and excessive block placements. With OaExploits, you can set chunk limits, control commands, and monitor server stats—all with extensive configuration options.

#### Key Features:

1. **Illegal Items Management**:
   - Automatically detects and removes illegal items from players' inventories and containers.
   - Supports a comprehensive list of configurable illegal items such as command blocks, bedrock, barriers, and more.
   
   Example of configurable illegal items:
   ```yaml
   illegal-items:
     blocks:
     - CHAIN_COMMAND_BLOCK
     - COMMAND_BLOCK
     - COMMAND_BLOCK_MINECART
     - REPEATING_COMMAND_BLOCK
     - BEDROCK
     - BARRIER
     - STRUCTURE_BLOCK
     - STRUCTURE_VOID
     - NETHER_PORTAL
     - LIGHT
     - END_PORTAL_FRAME
     - END_PORTAL
     - SPAWNER
   ```

2. **Chunk Limiter**:
   - Set limits for specific items within each chunk to prevent excessive block placement and potential server lag.
   - Fully customizable messages to inform players when they exceed these limits.
   
   Example of chunk limiter configuration:
   ```yaml
   chunk-limiter:
     limits:
       CHEST: 400
       TRAPPED_CHEST: 400
       TNT: 200
     
     messages:
       block-limit-exceeded: You cannot place more than {limit} {block} blocks in this chunk.
   ```

3. **Command Control**:
   - Block specific commands and create a whitelist of allowed commands to control server operations.
   - Improve server security by preventing unauthorized command usage.

   Examples of command whitelist and blacklist:
   ```yaml
   command-whitelist:
     enabled: true
     commands:
     - help
     - vote
     - joindate
     # ... other commands
     
   command-blacklist:
     enabled: true
     commands:
     - op
     - deop
     - plugins
     - pl
     # ... other commands
   ```

4. **Customizable Notifications**:
   - Notify players with customizable messages when they attempt to place or interact with illegal items.
   - Tailor messages to fit your server's style and rules.
   
   Example of customizable messages:
   ```yaml
   messages:
     illegal-item-placement:
       title: '&cIllegal Block!'
       subtitle: '&cYou cannot place that block!'
     illegal-item-interaction:
       title: '&cIllegal Item!'
       subtitle: '&cYou tried to interact with an illegal item: %item%'
     # ... other messages
   ```

5. **Built-in /stats Command**:
   - Provides comprehensive world statistics for server admins and players.
   - Useful for monitoring server health and player activities.

6. **Admin Alerts**:
   - Sends alerts to admins when players attempt to interact with illegal items.
   - Prevents abuse and keeps server administrators informed.
   
   Example of admin alerts configuration:
   ```yaml
   admin-alerts:
     enabled: true
     permission: oaexploits.alerts
     cooldown: 60 # seconds between alerts to avoid spam
   ```

7. **Deop on Leave**:
   - Automatically deops players upon leaving the server.
   - Optional teleportation to a specific location and customizable messages.
   
   Example of deop on leave configuration:
   ```yaml
   deop-on-leave:
     enabled: true
     whitelist:
       enabled: false
       players:
       - playername1
       - playername2
     teleport:
       world: world
       x: 0.0
       y: 64.0
       z: 0.0
       yaw: 0.0
       pitch: 0.0
     message: '&cYou have been deopped, your inventory cleared, and you have been teleported to the spawn point.'
   ```

8. **Logging and Debugging**:
   - Log illegal item actions with configurable log levels and files.
   - Enable debug mode to see what commands players are executing.

   Example of logging and debug settings:
   ```yaml
   log-settings:
     log-illegal-item-actions: true
     log-file: logs/oaexploits.log
     log-level: WARNING
     
   debug-mode: true
   ```

#### Installation and Usage:

1. **Download and Install**: Download the plugin from https://github.com/fanlimgames/oaexploits/releases  and place it in your server's plugins folder.
2. **Configure**: Edit the `config.yml` file to suit your server's requirements.
3. **Start Your Server**: Restart your server to load the plugin.
4. **Enjoy**: Your server is now protected with OaExploits!

Whether you run a large anarchy server or a small private server, OaExploits helps you maintain order and prevent exploitation. Download now and enhance your server's security and fairness!
