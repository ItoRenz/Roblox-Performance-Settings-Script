# 🎮 Roblox Performance Settings v3.5

A modern, sleek graphics settings GUI for Roblox games with real-time FPS monitoring and persistent quality preferences.

![Version](https://img.shields.io/badge/version-3.5-blue)
![Platform](https://img.shields.io/badge/platform-Roblox-red)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

- **4 Graphics Presets**: Cinematic, High, Medium, Low
- **Real-time FPS Counter**: Monitor your game performance
- **Persistent Settings**: Your preferences are saved across sessions
- **Mobile & Desktop Optimized**: Responsive UI for all devices
- **Modern UI Design**: Clean, minimalist interface with smooth animations
- **Color-Coded Indicators**: Each quality preset has its unique color
- **Instant Apply**: Graphics settings apply immediately without lag
- **Dynamic Particle Control**: Automatically manages new particles spawned in-game

## 📋 Quality Presets

### 🟣 Cinematic (Default)
- **Render Distance**: 2500 studs
- **Technology**: Future Lighting
- **Shadows**: Enabled
- **Post Processing**: Full (Bloom, Sun Rays, Color Correction, Atmosphere)
- **Particles**: Enabled
- **Best for**: Screenshots, cinematics, high-end PCs

### 🟢 High
- **Render Distance**: 1800 studs
- **Technology**: Future Lighting
- **Shadows**: Enabled
- **Post Processing**: Enhanced (Bloom, Sun Rays, Color Correction)
- **Particles**: Enabled
- **Best for**: Gaming with great visuals

### 🟠 Medium
- **Render Distance**: 900 studs
- **Technology**: ShadowMap
- **Shadows**: Enabled
- **Post Processing**: Basic (Bloom, Color Correction)
- **Particles**: Enabled
- **Best for**: Balanced performance and quality

### 🔴 Low
- **Render Distance**: 300 studs
- **Technology**: Legacy
- **Shadows**: Disabled
- **Post Processing**: Disabled
- **Particles**: Disabled
- **Best for**: Maximum FPS, low-end devices

## 🚀 Installation

1. Open your Roblox game in **Roblox Studio**
2. Navigate to **StarterPlayer > StarterPlayerScripts**
3. Create a new **LocalScript**
4. Copy and paste the entire script code
5. Rename the script to `PerformanceSettings` (optional)
6. Test your game!

## 🎯 Usage

### Opening the Settings Panel
- Click the **⚙** (gear) button on the right side of the screen
- The panel will appear in the top-right corner

### Changing Graphics Quality
1. Open the settings panel
2. Click on your desired quality preset:
   - **CINEMATIC** - Maximum visual quality
   - **HIGH** - Great visuals with good performance
   - **MEDIUM** - Balanced settings
   - **LOW** - Maximum performance
3. Settings apply instantly!
4. On mobile, the panel auto-closes after selection

### Monitoring Performance
- **FPS Counter** displays your current frames per second
- Color changes based on performance:
  - 🟢 Green: 55+ FPS (Excellent)
  - 🟡 Yellow: 30-54 FPS (Good)
  - 🔴 Red: Below 30 FPS (Poor)

## 📱 Platform Support

### Desktop
- Panel Size: 200x260 pixels
- Position: Top-right corner
- Toggle Button: Right side (slightly below center)
- Hover effects enabled

### Mobile
- Panel Size: 140x200 pixels (compact)
- Position: Top-right corner
- Toggle Button: Right side
- Auto-close after selection
- Touch-optimized buttons

## ⚙️ Technical Details

### Performance Optimizations
- **Debounced Operations**: Prevents excessive function calls
- **Batch Processing**: Parts are processed in batches to avoid lag
- **Async Tasks**: Heavy operations run asynchronously
- **Queue System**: Prevents concurrent quality changes

### Persistence
- Settings are saved using Player Attributes
- Automatically loads last used quality on respawn
- Survives game restarts

### Dynamic Updates
- Automatically applies settings to newly spawned particles
- Handles character respawns gracefully
- Cleans up resources on player removal

## 🎨 Customization

### Changing Colors
Edit the `COLORS` table to customize preset colors:
```lua
local COLORS = {
	Low = Color3.fromRGB(255, 100, 100),      -- Red
	Medium = Color3.fromRGB(255, 180, 60),    -- Orange
	High = Color3.fromRGB(100, 200, 100),     -- Green
	Cinematic = Color3.fromRGB(138, 43, 226)  -- Purple
}
```

### Adjusting Panel Position
Modify the `mainFrame.Position` values:
```lua
-- Desktop
mainFrame.Position = UDim2.new(1, -205, 0, 100)

-- Mobile
mainFrame.Position = UDim2.new(1, -145, 0, 80)
```

### Changing Default Quality
Edit the `currentQuality` variable:
```lua
local currentQuality = "High"  -- Options: "Low", "Medium", "High", "Cinematic"
```

## 🐛 Troubleshooting

### Panel doesn't appear
- Ensure the script is in `StarterPlayer > StarterPlayerScripts`
- Check if it's a **LocalScript** (not a regular Script)
- Look for errors in the Output window

### Settings don't apply
- Check the Output console for error messages
- Ensure your game has proper lighting objects
- Try restarting the test server

### FPS counter shows "--"
- Wait a few seconds for initialization
- The counter updates every 0.5 seconds

### Settings don't save
- Player Attributes must be enabled in your game
- Check if DataStore is configured properly

## 📊 Version History

### v3.5 (Current)
- ✅ Set Cinematic as default quality
- ✅ Reordered buttons: Cinematic → High → Medium → Low
- ✅ Fixed close button icon (changed from ✕ to X)
- ✅ Repositioned panel to top-right corner
- ✅ Fixed layout order for proper button arrangement
- ✅ Enhanced UI with color-coded stroke indicators
- ✅ Added dot indicators for active preset
- ✅ Improved hover animations

### v3.4
- Modern minimalist design
- Instant close button response
- Clean accent bars for active preset
- Mobile optimized compact size

### v3.0
- Complete UI redesign
- Added persistent settings
- Improved FPS counter
- Better mobile support

## 📝 License

This script is free to use in any Roblox game. Attribution is appreciated but not required.

## 🤝 Contributing

Feel free to modify and improve this script! If you create an enhanced version, consider sharing it with the community.

## 💡 Credits

Created for the Roblox development community

---

**Need help?** Check the Roblox Developer Forum or DevHub for additional support.

**Enjoying this script?** Give it a ⭐ and share it with other developers!
