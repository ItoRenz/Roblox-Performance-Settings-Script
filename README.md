# ⚡ ROBLOX Performance Settings Script

A feature-rich, animated performance settings GUI for ROBLOX games with smooth transitions and multiple quality presets.

![ROBLOX](https://img.shields.io/badge/ROBLOX-000000?style=for-the-badge&logo=roblox&logoColor=white)
![Lua](https://img.shields.io/badge/Lua-2C2D72?style=for-the-badge&logo=lua&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## ✨ Features

### 🎮 Quality Presets
- **Low** - Optimized for maximum FPS (250 render distance, no shadows)
- **Medium** - Balanced performance (800 render distance, basic shadows)
- **High** - Enhanced visuals (1500 render distance, full effects)
- **Cinematic** - Maximum quality (2500 render distance, all effects enabled)

### 🎨 Animated Toggle Button
- **Pulse Effect** - Glowing border animation on hover
- **Breathing Animation** - Subtle size pulsing when idle
- **Hover Effects** - Smooth color and scale transitions
- **Click Animation** - Bounce effect with squeeze and expand
- **Edge Positioning** - Stays at screen edge, doesn't obstruct gameplay

### 📊 Real-time Monitoring
- **FPS Counter** - Live frame rate display with color indicators
  - 🟢 Green: 55+ FPS
  - 🟡 Yellow: 30-54 FPS
  - 🔴 Red: Below 30 FPS
- **Current Quality Display** - Shows active preset

### 🔧 Graphics Settings Control
- Render distance adjustment
- Shadow quality (Global + Per-Part)
- Particle effects toggle
- Post-processing effects (Bloom, SunRays, DoF, Atmosphere)
- Lighting technology (Legacy/ShadowMap/Future)
- Fog control
- Material reflectance
- Environment lighting scales

### 💾 Smart Features
- **Auto-save** - Remembers your quality preference
- **Auto-apply** - Reapplies settings on respawn
- **Batch Processing** - Efficient part processing to prevent lag
- **Mobile Support** - Optimized UI for touch devices
- **Desktop Hotkey** - Press `G` to toggle menu
- **Queue System** - Prevents spam clicks and conflicts

## 📦 Installation

### Method 1: Direct Copy
1. Open **ROBLOX Studio**
2. Navigate to `StarterPlayer` → `StarterPlayerScripts`
3. Create a new **LocalScript**
4. Copy the entire script from `PerformanceSettings.lua`
5. Paste into the LocalScript
6. Save and test!

### Method 2: Model Import
1. Download the `.rbxm` model file (if available)
2. Right-click `StarterPlayerScripts` in Explorer
3. Select "Insert from File"
4. Choose the downloaded model

## 🎯 Usage

### Desktop
- Click the **⚙️ button** on the right edge of screen
- Or press **G key** to toggle menu
- Select your desired quality preset
- Settings apply automatically

### Mobile
- Tap the **⚙️ button** on the right edge
- Choose quality preset
- Menu auto-closes after selection

## 🎨 Customization

### Change Colors
```lua
local COLORS = {
    Low = Color3.fromRGB(255, 100, 100),      -- Red
    Medium = Color3.fromRGB(255, 180, 60),    -- Orange
    High = Color3.fromRGB(100, 200, 100),     -- Green
    Cinematic = Color3.fromRGB(138, 43, 226)  -- Purple
}
```

### Adjust Quality Presets
```lua
local QUALITY_PRESETS = {
    Low = { 
        renderDistance = 250,
        shadowsEnabled = false,
        particlesEnabled = false,
        -- Add more settings...
    }
}
```

### Change Hotkey
```lua
if input.KeyCode == Enum.KeyCode.G then  -- Change G to any key
    screenGui.Enabled = not screenGui.Enabled
end
```

### Modify Animation Speed
```lua
-- Breathing speed
local time = tick() * 1.5  -- Change 1.5 to adjust speed

-- Pulse speed
local time = tick() * 2  -- Change 2 to adjust speed
```

## 🔧 Technical Details

### Performance Optimizations
- **Debouncing** - Prevents rapid-fire function calls
- **Batch Processing** - Processes parts in groups of 100
- **Task Spawning** - Async operations don't block main thread
- **Queue System** - Prevents setting conflicts
- **pcall Protection** - Error handling prevents crashes

### Compatibility
- ✅ Desktop (Windows, Mac)
- ✅ Mobile (iOS, Android)
- ✅ Tablet
- ✅ All ROBLOX client versions
- ✅ Works in all games (no special permissions needed)

## 📸 Screenshots

### Toggle Button States
```
Idle:     Breathing animation (subtle pulse)
Hover:    Glow effect + scale 1.1x
Click:    Bounce animation (squeeze → expand)
```

### Quality Comparison
| Setting | Render Dist | Shadows | Particles | Post FX | Avg FPS |
|---------|------------|---------|-----------|---------|---------|
| Low | 250 | ❌ | ❌ | ❌ | 60+ |
| Medium | 800 | ✅ | ✅ | ❌ | 50-60 |
| High | 1500 | ✅ | ✅ | ✅ | 35-50 |
| Cinematic | 2500 | ✅ | ✅ | ✅✅ | 25-35 |

## 🐛 Troubleshooting

### Button Not Appearing
- Check if script is in `StarterPlayerScripts`
- Verify it's a `LocalScript`, not a regular Script
- Check Output for error messages

### Settings Not Applying
- Wait 2 seconds after joining (auto-apply delay)
- Check if game has custom lighting settings
- Some games may override settings

### FPS Not Updating
- This is normal - updates every 0.5 seconds
- Check if `RunService` is accessible

### Animations Laggy
- Reduce animation speed multipliers
- Disable breathing animation if needed
- Check overall game performance

## 📝 Changelog

### Version 2.0 (Current)
- ✨ Added animated toggle button
- 🎨 Pulse effect on hover
- 💫 Breathing animation when idle
- 🎯 Bounce animation on click
- 🔧 Improved mobile support
- 🐛 Fixed edge positioning issues

### Version 1.0
- 🎮 Initial release
- ⚙️ 4 quality presets
- 📊 FPS counter
- 💾 Auto-save settings

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### How to Contribute
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- ROBLOX Developer Hub for API documentation
- Community feedback and suggestions
- TweenService for smooth animations

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/yourusername/roblox-performance-settings/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/roblox-performance-settings/discussions)
- **ROBLOX DevForum**: [Link to thread]

## ⭐ Star History

If you find this useful, please consider giving it a star! ⭐

---

Made with ❤️ for the ROBLOX community
