# 🎮 Roblox Performance Settings Script v3.5

**Author:** ItoRenz00

A comprehensive graphics quality manager for Roblox games with real-time FPS monitoring, dynamic performance optimization, and an intuitive UI for both desktop and mobile platforms.

---

## ✨ Features

- **4 Quality Presets**: Low, Medium, High, and Cinematic
- **Real-time FPS Counter**: Monitor performance with color-coded indicators
- **Auto-save Settings**: Preferences persist across game sessions
- **Mobile & Desktop Support**: Responsive UI optimized for all platforms
- **Dynamic Particle Management**: Automatically handles new particles
- **Smooth Animations**: Polished UI with hover effects and transitions
- **Color-coded Indicators**: Visual feedback for each quality level
- **Batch Processing**: Efficient performance optimization
- **Auto-apply on Spawn**: Settings automatically apply when character respawns

---

## 📋 Quality Presets

### 🔴 Low Quality
- **Render Distance**: 300 studs
- **Shadows**: Disabled
- **Particles**: Disabled
- **Post Processing**: Disabled
- **Technology**: Legacy
- **Best for**: Low-end devices, maximum FPS

### 🟠 Medium Quality
- **Render Distance**: 900 studs
- **Shadows**: Enabled
- **Particles**: Enabled
- **Post Processing**: Basic bloom
- **Technology**: ShadowMap
- **Best for**: Mid-range devices, balanced performance

### 🟢 High Quality
- **Render Distance**: 1800 studs
- **Shadows**: Enabled
- **Particles**: Enabled
- **Post Processing**: Bloom + SunRays
- **Technology**: Future
- **Best for**: High-end devices, great visuals

### 🟣 Cinematic Quality
- **Render Distance**: 2500 studs
- **Shadows**: Enabled
- **Particles**: Enabled
- **Post Processing**: Full (Bloom, SunRays, Atmosphere, Color Correction)
- **Technology**: Future
- **Best for**: Screenshots, recordings, ultra-high-end devices

---

## 🚀 Installation

### Method 1: Roblox Studio
1. Open your game in Roblox Studio
2. Navigate to `StarterPlayer` > `StarterPlayerScripts`
3. Create a new `LocalScript`
4. Copy and paste the entire script code
5. Rename the script to `PerformanceSettings` (optional)
6. Test in-game

### Method 2: Command Bar
1. Open Roblox Studio
2. Go to `View` > `Command Bar`
3. Paste the script and execute
4. The script will auto-configure

---

## 🎯 Usage

### Opening Settings Panel
- **Desktop**: Click the ⚙️ button on the right side of the screen
- **Mobile**: Tap the ⚙️ button on the right side of the screen

### Changing Quality
1. Open the settings panel
2. Select your desired quality preset:
   - **Cinematic** (Purple)
   - **High** (Green)
   - **Medium** (Orange)
   - **Low** (Red)
3. Wait for the settings to apply
4. Monitor FPS to ensure optimal performance

### FPS Monitoring
- **Green FPS (≥55)**: Excellent performance
- **Orange FPS (30-54)**: Acceptable performance
- **Red FPS (<30)**: Poor performance, consider lowering quality

---

## 🛠️ Configuration

### Customizing Quality Presets

Edit the `QUALITY_PRESETS` table to customize settings:

```lua
local QUALITY_PRESETS = {
    Custom = {
        renderDistance = 1500,
        shadowsEnabled = true,
        particlesEnabled = true,
        postProcessing = true,
        fogEnabled = false,
        brightness = 2.5,
        technology = Enum.Technology.Future,
        -- Add more settings...
    }
}
```

### Changing Default Quality

Modify this line to change the default quality:

```lua
local currentQuality = "Cinematic"  -- Change to "High", "Medium", or "Low"
```

### Adjusting UI Position

For desktop:
```lua
mainFrame.Position = UDim2.new(1, -205, 0, 100)  -- Adjust values
```

For mobile:
```lua
mainFrame.Position = UDim2.new(1, -145, 0, 80)  -- Adjust values
```

---

## 📱 Platform Compatibility

### Desktop
- Full-featured UI with hover effects
- Keyboard and mouse support
- Larger, more detailed interface

### Mobile
- Touch-optimized controls
- Compact UI for smaller screens
- Auto-close after selection
- Optimized button sizes

---

## 🔧 Technical Details

### Performance Optimization
- **Batch Processing**: Processes objects in chunks to prevent lag
- **Debouncing**: Prevents rapid repeated function calls
- **Queue System**: Manages multiple quality changes efficiently
- **Async Operations**: Uses task.spawn() for non-blocking operations

### Memory Management
- Automatic cleanup on player removal
- Proper connection disposal
- Efficient event handling

### Error Handling
- Wrapped in pcall() for safe execution
- Graceful degradation on errors
- Console logging for debugging

---

## 📊 Performance Impact

| Quality | FPS (Low-End) | FPS (Mid-Range) | FPS (High-End) |
|---------|---------------|-----------------|----------------|
| Low     | 50-60         | 60              | 60             |
| Medium  | 30-45         | 50-60           | 60             |
| High    | 20-35         | 40-55           | 55-60          |
| Cinematic| 15-25        | 30-45           | 50-60          |

*Results may vary depending on game complexity*

---

## 🐛 Troubleshooting

### Settings Not Saving
- Check if PlayerAttributes are enabled in your game
- Ensure the script has proper permissions

### UI Not Appearing
- Verify script is in `StarterPlayerScripts`
- Check for script errors in Output window
- Ensure ResetOnSpawn is false

### Low FPS After Applying Settings
- Try a lower quality preset
- Close other applications
- Check your device specifications

### Toggle Button Not Responsive
- Wait for initial load (2 seconds)
- Refresh the game
- Check for script conflicts

---

## 🔄 Version History

### v3.5 (Current)
- Enhanced UI with color-coded indicators
- Improved mobile responsiveness
- Added smooth animations and hover effects
- Better error handling
- Optimized batch processing
- Added quality indicator dots

### v3.0
- Added Cinematic quality preset
- Implemented FPS counter
- Mobile optimization
- Auto-save functionality

### v2.0
- Added GUI interface
- Multiple quality presets
- Dynamic particle handling

### v1.0
- Initial release
- Basic performance settings

---

## 📝 License

This script is provided as-is for use in Roblox games. Feel free to modify and distribute, but please credit the original author.

---

## 👤 Author

**ItoRenz00**

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📞 Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Contact the author
- Check the troubleshooting section

---

## ⭐ Acknowledgments

- Thanks to the Roblox developer community
- Inspired by various performance optimization techniques
- Built with modern UI/UX principles

---

## 📄 Changelog

See [CHANGELOG.md](CHANGELOG.md) for detailed version history.

---

**Made with ❤️ by ItoRenz00**
