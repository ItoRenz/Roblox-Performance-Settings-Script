# ⚡ Roblox Performance Settings Script

A comprehensive, user-friendly graphics settings manager for Roblox games. Give players full control over their visual experience with 4 optimized quality presets, real-time FPS monitoring, and an elegant UI that works seamlessly on both desktop and mobile.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Roblox](https://img.shields.io/badge/roblox-compatible-brightgreen)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

### 🎮 Four Quality Presets
- **Low** - Maximum performance for low-end devices
- **Medium** - Balanced graphics and performance
- **High** - Enhanced visuals with good performance
- **Ultra** - Cinematic quality with all effects enabled

### 📊 Real-Time Monitoring
- Live FPS counter with color-coded performance indicators
- Automatic quality persistence across game sessions
- Visual feedback for current settings

### 🎨 Advanced Graphics Control
- Dynamic render distance adjustment (250-2500 studs)
- Quality levels from 1-21
- Shadow and lighting technology switching
- Particle effects management
- Post-processing effects (Bloom, SunRays, Color Correction)
- Atmospheric effects (Ultra only)
- Depth of Field (Ultra only)
- Material reflectance control
- Ambient lighting customization

### 📱 Cross-Platform Support
- Responsive UI for desktop and mobile
- Touch-optimized interface for mobile devices
- Keyboard shortcut (G key) for desktop users
- Adaptive sizing and positioning

### 🎯 User Experience
- Sleek, modern dark-themed interface
- Color-coded quality buttons
- Smooth animations and hover effects
- Auto-hide on mobile after selection
- Settings toggle button always accessible

## 📥 Installation

### Method 1: Direct Script
1. Open Roblox Studio
2. Navigate to `StarterPlayer` > `StarterPlayerScripts`
3. Create a new `LocalScript`
4. Copy and paste the entire script code
5. Rename the script to `PerformanceSettings` (optional)
6. Save and publish your game

### Method 2: Model Insert
1. Get the model from Roblox Library (if published)
2. Insert into your game
3. The script will automatically be placed in `StarterPlayerScripts`

## 🎮 Usage

### For Players

#### Desktop
- Press **G** key to open/close settings menu
- Click the **⚙️** button on the right side of screen
- Select your preferred quality preset
- Monitor your FPS in real-time

#### Mobile
- Tap the **⚙️** button on the right edge
- Select quality preset (menu auto-closes)
- Check FPS at the top of the settings panel

### For Developers

#### Customization
The script is highly customizable. Key configuration options:

```lua
-- Adjust render distances
renderDistance = 250  -- Minimum distance for Low preset

-- Modify quality levels
qualityLevel = Enum.QualityLevel.Level21  -- Maximum quality

-- Toggle features
shadowsEnabled = true
particlesEnabled = true
postProcessing = true
```

#### Hotkey Configuration
Change the default hotkey (G) by modifying:
```lua
if input.KeyCode == Enum.KeyCode.G then
    -- Change to any KeyCode
end
```

## 🔧 Technical Details

### Performance Impact by Preset

| Preset | Render Distance | Quality Level | Shadows | Particles | Post FX | Expected FPS Gain |
|--------|----------------|---------------|---------|-----------|---------|-------------------|
| Low    | 250 studs      | Level 01      | ❌      | ❌        | ❌      | +40-60 FPS        |
| Medium | 800 studs      | Level 08      | ✅      | ✅        | ❌      | +20-30 FPS        |
| High   | 1500 studs     | Level 15      | ✅      | ✅        | ✅      | Baseline          |
| Ultra  | 2500 studs     | Level 21      | ✅      | ✅        | ✅✅    | -10-20 FPS        |

### Graphics Features Breakdown

#### Low Preset
- Legacy lighting technology
- Fog enabled for performance
- Minimal ambient lighting (30%)
- No shadows or reflections
- Ideal for: Mobile devices, low-end PCs

#### Medium Preset
- ShadowMap technology
- Basic shadows enabled
- Particles active
- 30% reflectance
- Ideal for: Mid-range devices

#### High Preset
- Future lighting technology
- Enhanced post-processing
- Bloom and SunRays effects
- Color correction
- 60% reflectance
- Ideal for: Good gaming PCs

#### Ultra Preset
- Maximum quality (Level 21)
- Full atmospheric system
- Depth of Field effect
- Enhanced bloom and blur
- 100% reflectance
- Cinematic color grading
- Ideal for: High-end gaming setups

## 🎨 Visual Differences

### Post-Processing Effects

**High Quality:**
- Bloom: Intensity 0.5, Size 32
- SunRays: Intensity 0.04
- Color Correction: Subtle enhancement

**Ultra Quality:**
- Bloom: Intensity 1.0, Size 56
- SunRays: Intensity 0.08
- Enhanced Color Correction with warm tint
- Atmosphere with haze and decay
- Depth of Field for cinematic blur
- Overall blur for depth perception

## 📋 Requirements

- Roblox Studio (latest version recommended)
- Game must allow client-side scripts
- No additional plugins required

## ⚠️ Known Limitations

- Settings reset on game rejoin (by design for performance)
- Some effects may not work in certain lighting conditions
- Ultra preset may cause lag on low-end devices
- Mobile devices may have reduced effect visibility

## 🔄 Auto-Apply Features

The script automatically:
- Reapplies settings on character respawn
- Manages new particles added to workspace
- Saves player's preferred quality
- Adjusts shadows on new parts
- Updates reflectance on materials

## 🐛 Troubleshooting

**Settings not applying?**
- Check if script is in `StarterPlayerScripts`
- Ensure LocalScript is enabled
- Check for script errors in Output window

**FPS counter showing "--"?**
- Wait 0.5 seconds for initial calculation
- Verify RenderStepped is not blocked

**UI not showing?**
- Check if ScreenGui is enabled
- Verify PlayerGui is accessible
- Press G (desktop) or look for ⚙️ button

**Performance not improving?**
- Some games have minimum quality settings
- Server performance may affect overall FPS
- Check if game has forced quality settings

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs via Issues
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is licensed under the MIT License - feel free to use it in your Roblox games!

## 🌟 Credits

Created with ❤️ for the Roblox developer community

## 📞 Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Check the troubleshooting section
- Review Roblox DevForum for similar topics

## 🔮 Future Updates

Planned features:
- [ ] Custom preset creation
- [ ] Graphics benchmarking tool
- [ ] Auto-quality adjustment based on FPS
- [ ] More post-processing options
- [ ] Settings export/import
- [ ] Admin controls for forced quality

---

**⭐ If this script helped your game, consider giving it a star!**

**Made for Roblox developers who care about player experience** 🎮
