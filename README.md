# 🎮 Roblox Performance Settings Script

A comprehensive graphics quality management script for Roblox games with a sleek GUI interface. This script allows players to adjust visual settings in real-time to optimize their gameplay experience based on their device capabilities.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Roblox](https://img.shields.io/badge/Platform-Roblox-blue.svg)](https://www.roblox.com/)
[![Lua](https://img.shields.io/badge/Language-Lua-purple.svg)](https://www.lua.org/)

## ✨ Features

### 🎨 Four Quality Presets
- **Low** - Optimized for low-end devices and maximum FPS
- **Medium** - Balanced performance and visuals
- **High** - Enhanced graphics for capable devices
- **Cinematic** - Premium visual experience with advanced effects

### 🔧 Comprehensive Graphics Control
- **Render Distance** - Adjustable camera zoom distance
- **Shadow System** - Global and per-part shadow control
- **Particle Effects** - Dynamic particle emitter management
- **Post-Processing** - Bloom, SunRays, Color Correction, DoF, and more
- **Lighting Technology** - Legacy, ShadowMap, and Future lighting
- **Fog System** - Distance-based fog effects
- **Reflectance** - Material reflectivity adjustment
- **Ambient Lighting** - Environment lighting customization

### 📊 Real-Time Monitoring
- **FPS Counter** - Live frame rate display with color-coded performance
- **Status Indicator** - Current quality preset display

### 💾 Quality Persistence
- Automatically saves and restores user preferences
- Settings persist across respawns

### 📱 Cross-Platform Support
- **Desktop**: Hotkey (G) and click-to-toggle
- **Mobile**: Touch-optimized UI with scaled controls
- Auto-detection of device type

### ⚡ Performance Optimizations
- Batch processing for large-scale object modifications
- Debounced event handlers to prevent lag
- Queue system for setting changes
- Efficient FPS calculation
- Yielding during intensive operations

## 📥 Installation

### Method 1: Direct Insertion
1. Open your Roblox game in Roblox Studio
2. Navigate to `StarterPlayer` → `StarterPlayerScripts`
3. Create a new `LocalScript`
4. Copy and paste the entire script code
5. Rename the script to `PerformanceSettings` (optional)
6. Test in Play mode

### Method 2: Model Import
1. Download the script file
2. In Roblox Studio, go to `View` → `Toolbox`
3. Click `Import 3D` or use `File` → `Insert from File`
4. Select the downloaded file
5. Move the script to `StarterPlayer` → `StarterPlayerScripts`

## 🎯 Usage

### For Desktop Players
- **Open Settings**: Press `G` key or click the ⚙️ button on the right edge
- **Select Quality**: Click on Low, Medium, High, or Cinematic
- **Close Menu**: Click the ✕ button or press `G` again

### For Mobile Players
- **Open Settings**: Tap the ⚙️ button on the right edge
- **Select Quality**: Tap on your desired quality preset
- **Auto-Close**: Menu automatically closes after selection

### Quality Preset Details

| Preset | Render Distance | Shadows | Particles | Post-Processing | Best For |
|--------|----------------|---------|-----------|-----------------|----------|
| **Low** | 250 studs | ❌ | ❌ | ❌ | Low-end devices, maximum FPS |
| **Medium** | 800 studs | ✅ | ✅ | ❌ | Balanced gameplay |
| **High** | 1500 studs | ✅ | ✅ | ✅ | High-performance PCs |
| **Cinematic** | 2500 studs | ✅ | ✅ | ✅✅ | Screenshots, recordings |

## ⚙️ Configuration

You can customize the script by modifying the `QUALITY_PRESETS` table:

```lua
local QUALITY_PRESETS = {
    CustomQuality = {
        renderDistance = 1000,      -- Camera max zoom distance
        shadowsEnabled = true,       -- Global shadows on/off
        particlesEnabled = true,     -- Particle emitters on/off
        postProcessing = false,      -- Post effects on/off
        fogEnabled = false,          -- Distance fog on/off
        brightness = 2,              -- Lighting brightness (1-3)
        technology = Enum.Technology.ShadowMap,
        castShadow = true,           -- Per-part shadows
        reflectance = 0.3,           -- Material reflectance (0-1)
        -- ... other settings
    }
}
```

### Customizing Colors
Modify the `COLORS` table to change button colors:

```lua
local COLORS = {
    Low = Color3.fromRGB(255, 100, 100),
    Medium = Color3.fromRGB(255, 180, 60),
    High = Color3.fromRGB(100, 200, 100),
    Cinematic = Color3.fromRGB(138, 43, 226)
}
```

### Changing Hotkey (Desktop)
Find this line and change `Enum.KeyCode.G` to your preferred key:

```lua
if input.KeyCode == Enum.KeyCode.G then
```

## 🛠️ Technical Details

### System Requirements
- **Roblox Studio** version 2019 or later
- **FilteringEnabled** must be enabled
- **LocalScript** execution in `StarterPlayerScripts`

### Services Used
- `Players` - Player management
- `RunService` - FPS calculation
- `UserInputService` - Input detection
- `Lighting` - Visual effects
- `Workspace` - Object manipulation

### Performance Impact
- **Low overhead** - Minimal impact on game performance
- **Optimized loops** - Batch processing prevents lag spikes
- **Event debouncing** - Prevents excessive function calls
- **Smart caching** - Reduces redundant operations

## 🔍 Troubleshooting

### Common Issues

**Settings not applying:**
- Ensure the script is in `StarterPlayer` → `StarterPlayerScripts`
- Check that it's a `LocalScript`, not a regular Script
- Verify FilteringEnabled is enabled

**GUI not showing:**
- Check if PlayerGui is accessible
- Ensure ResetOnSpawn is set to false
- Look for errors in Output window

**FPS counter stuck:**
- RenderStepped connection may have failed
- Check for script errors in Output

**Settings reset on respawn:**
- This is intentional - settings are reapplied automatically
- Preferences are saved and restored

## 📝 Changelog

### Version 1.0.0 (Current)
- ✅ Initial release
- ✅ Four quality presets
- ✅ Real-time FPS counter
- ✅ Cross-platform support
- ✅ Quality persistence
- ✅ Batch processing optimization
- ✅ Auto-application on respawn

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Create** a new branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Ideas for Contributions
- Additional quality presets
- More post-processing effects
- Advanced graphics settings
- Settings export/import
- UI themes
- Localization support

## 📄 License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 💬 Support

- **Issues**: Report bugs via [GitHub Issues](https://github.com/yourusername/roblox-performance-settings/issues)
- **Discussions**: Ask questions in [Discussions](https://github.com/yourusername/roblox-performance-settings/discussions)
- **Roblox DevForum**: [Post your questions](https://devforum.roblox.com/)

## 🌟 Credits

Created with ❤️ for the Roblox development community

### Special Thanks
- Roblox Developer Community
- Contributors and testers
- Everyone who uses this script

## 📚 Resources

- [Roblox Developer Hub](https://create.roblox.com/docs)
- [Roblox API Reference](https://create.roblox.com/docs/reference/engine)
- [Lighting Effects Guide](https://create.roblox.com/docs/environment/lighting)
- [Performance Optimization](https://create.roblox.com/docs/optimization)

---

⭐ **If you find this useful, please consider giving it a star!** ⭐

Made for Roblox developers by Roblox developers 🎮
