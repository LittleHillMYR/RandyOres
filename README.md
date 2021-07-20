# <img src = "README.assets/randyores.png" alt = "RandyOres Logo" width = "35"> RandyOres
A mining economy plugin made for Spigot servers.

## Version compatibility
| Minecraft version | Compatibility                                                |
| ----------------- | ------------------------------------------------------------ |
| Below 1.13        | Unsupported due to `api-version` being set to `1.13`.        |
| 1.13              | Supported natively. Support will be dropped on Minecraft 1.18 update. |
| 1.14              | Supported.                                                   |
| 1.15              | Supported.                                                   |
| 1.16              | Supported.                                                   |
| 1.17              | Supported.                                                   |
| 1.18              | Will be supported not long after its Spigot stable release.  |

## Installation
1. Make sure you have [Vault](https://www.spigotmc.org/resources/vault.34315/) plugin, and an 
   economy system plugin installed.
2. Copy the plugin jar file into `/plugins` directory
3. Adjust the config file inside `/plugins/RandyOres` to your likings.
4. Enjoy!

## Config
### Settings
- `allowSilkTouch`
  - When true, players are able to get money when mining with silk touch enchanted pickaxe. 
  - Defaults to true
- `allowedSilkTouchBlocks`
  - A list of blocks that are immune to `allowSilkTouch`, that means these blocks will give money 
    even if player is mining with silk touch enchanted pickaxe.
  - Must be in YAML list form for system to recognize.
    ```yaml
    # Option 1
    allowedSilkTouchBlocks:
      - STONE
      - COAL_ORE
    
    # Option 2
    allowedSilkTouchBlocks: [STONE, COAL_ORE]
    ```
  - Defaults to null
- `allowCreativeMode`
  - When true, players are able to get money when breaking blocks in creative mode.
  - Defaults to false.
  
### Blocks
Under this key should be lines of `String` to `Integer` key-value pairs which its
`String` is a [block's enum name](https://papermc.io/javadocs/paper/1.17/org/bukkit/Material.html)
and `Integer` is the block's price. 

For example: 
```yaml
Blocks:
  BEACON: 100
  BRICK: 5
```

## Permissions
- `randyores.blockpermoney`
  - Allow players to get money when mining specific block.
  - Defaults to everyone