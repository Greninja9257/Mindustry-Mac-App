# Mindustry Mac App

A convenient wrapper that converts Mindustry JAR files into native Mac applications, enabling stable gameplay of unstable Mac versions.

## Overview

This project provides a Mac app bundle that allows you to run any version of Mindustry (including unstable/bleeding-edge versions) as a native macOS application. Instead of dealing with command-line Java execution, you can simply double-click to launch the game.

## What is Mindustry?

Mindustry is a factory-building tower defense game where you create elaborate supply chains to ammo, units and structures, then defend your structures from waves of enemies. Learn more at [mindustrygame.github.io](https://mindustrygame.github.io/).

## Features

- 🚀 Run any Mindustry version as a native Mac app
- 🔄 Easy version switching by replacing JAR files
- 📱 Proper macOS integration (dock icon, app switcher, etc.)
- 🛡️ Stable execution of unstable game versions
- ⚡ No command-line knowledge required

## Prerequisites

- **macOS 10.14 or later**
- **Java 17 or higher** installed on your system
  - Download from [Oracle](https://www.oracle.com/java/technologies/downloads/) or [OpenJDK](https://openjdk.org/)
  - Verify installation: `java -version` in Terminal

## Installation

### Quick Start
1. **Download** the latest release from the [Downloads section](../../releases)
2. **Move** the app to your Applications folder
3. **Launch** by double-clicking the app icon

### Updating Mindustry Version
1. **Right-click** the Mindustry app and select "Show Package Contents"
2. **Navigate** to `Contents/Resources/Java/`
3. **Replace** `Mindustry.jar` with your desired version
4. **Rename** the new JAR file to `Mindustry.jar`
5. **Launch** the app normally

## Where to Get Mindustry JAR Files

- **Stable releases**: [GitHub Releases](https://github.com/Anuken/Mindustry/releases)
- **Bleeding-edge builds**: [Mindustry Builds](https://github.com/Anuken/MindustryBuilds/releases)
- **Classic versions**: Available in the releases section

## Troubleshooting

### App Won't Launch
- **Check Java installation**: Run `java -version` in Terminal
- **Verify JAR file**: Ensure `Mindustry.jar` exists in `Contents/Resources/Java/`
- **Check permissions**: Try running `chmod +x /path/to/Mindustry.app/Contents/MacOS/JavaApplicationStub`

### Performance Issues
- **Allocate more memory**: Edit `Contents/Info.plist` and modify JVM options
- **Update Java**: Ensure you're using the latest Java version
- **Close other applications**: Free up system resources

### Security Warnings
- **First run**: macOS may show security warnings for unsigned apps
- **Solution**: Go to System Preferences > Security & Privacy and click "Open Anyway"
- **Alternative**: Right-click the app and select "Open"

## Advanced Configuration

### Custom JVM Arguments
Edit `Contents/Info.plist` to add custom Java arguments:
```xml
<key>JVMOptions</key>
<array>
    <string>-Xmx4G</string>
    <string>-Xms1G</string>
</array>
```

### App Icon Customization
Replace `Contents/Resources/icon.icns` with your preferred icon file.

## Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests.

### Development Setup
1. Clone this repository
2. Make your changes
3. Test with different Mindustry versions
4. Submit a pull request

## Support

- **Issues**: Report bugs or request features in the [Issues section](../../issues)
- **Community**: Join the Mindustry community on [Discord](https://discord.gg/mindustry)
- **Wiki**: Check the [Mindustry Wiki](https://mindustrygame.github.io/wiki/) for game-related help

## License

This project is provided as-is for the convenience of Mindustry players. Mindustry itself is licensed under GPL v3.

## Acknowledgments

- **Anuken** for creating Mindustry
- **The Mindustry community** for their continued support
- **Contributors** who help improve this wrapper

---

**Note**: This is an unofficial wrapper. For official support, visit the [Mindustry GitHub repository](https://github.com/Anuken/Mindustry).
**AnotherNote**: Don't use if there are official versions of the version you require.
**AnothernotherNote**: Contributions are welcome! The more versions available, the better! Feel free to help add versions, if I missed some!
