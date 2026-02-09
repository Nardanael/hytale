# HytaleMods

This directory contains modifications to the base Hytale game assets.

## Structure

The directory structure mirrors the `Assets` repository. To override a game file, create the same directory path under `HytaleMods` and place your modified file there.

## Current Modifications

### Shovel Double-Dig Feature

**File**: `Server/Item/Interactions/Weapons/Shovel/Attacks/Shovel_Dig.json`

**Description**: Modified the shovel interaction to dig two blocks vertically instead of one.

**Implementation**:
- Uses parallel selectors to target two blocks simultaneously
- First selector targets the primary block (standard behavior)
- Second selector targets the block below using vertical offset (ExtendTop: -0.5, ExtendBottom: 1.5)
- Both blocks are broken when the player uses the shovel

**Effect**: When using a shovel, it will dig both the targeted block and the block directly below it, making it more efficient for digging downward.

## How to Use

1. Place the `HytaleMods` directory in your Hytale mods folder
2. Ensure the directory structure matches the Assets structure exactly
3. The game will override the default Assets with files from HytaleMods

## File Override System

Only files that need modification are included in this directory. All other game assets remain unchanged and will be loaded from the base `Assets` directory.
