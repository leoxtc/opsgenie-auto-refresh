# Opsgenie Alert Auto Refresher

<div align="center">

![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-green?logo=googlechrome)
![Version](https://img.shields.io/badge/version-0.0.2-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Manifest](https://img.shields.io/badge/manifest-v3-orange)

*Automatically refresh Opsgenie alert pages to stay up-to-date with the latest incidents*

</div>

## 🚀 Overview

This Chrome extension automatically refreshes Opsgenie's Alert Page every 30 seconds, ensuring you never miss critical updates during incident response. 

**Why this extension exists:**
- Opsgenie has had a [pending feature request](https://jira.atlassian.com/browse/OPSGENIE-346) for years without implementation
- Due to Opsgenie's upcoming deprecation, this feature will likely never be officially added
- This is a community-maintained fork ensuring continued functionality

## ✨ Features

- 🔄 **Auto-refresh** - Refreshes alert pages every 30 seconds
- 🎯 **Smart targeting** - Only works on Opsgenie alert pages
- ⚡ **Lightweight** - Minimal resource usage
- 🔧 **Zero configuration** - Works immediately after installation
- 🛡️ **Safe** - No data collection or external requests

## 📥 Installation

### Option 1: Chrome Web Store (Recommended)
[![Chrome Web Store](https://img.shields.io/badge/Install%20from-Chrome%20Web%20Store-blue?logo=googlechrome)](https://chrome.google.com/webstore)

*Coming soon - extension is currently under review*

### Option 2: Manual Installation (Developer Mode)

1. **Download the extension**
   ```bash
   git clone https://github.com/yourusername/opsgenie-auto-refresher.git
   cd opsgenie-auto-refresher
   ```

2. **Load in Chrome**
   - Open Chrome and navigate to `chrome://extensions/`
   - Enable **Developer mode** (toggle in top-right corner)
   - Click **"Load unpacked"**
   - Select the extension folder

3. **Verify installation**
   - The extension icon should appear in your toolbar
   - Navigate to an Opsgenie alert page to test functionality

## 🔧 Usage

1. **Navigate to Opsgenie**
   - Go to any Opsgenie alert page (e.g., `https://yourcompany.app.opsgenie.com/alert/list`)

2. **Automatic operation**
   - The extension automatically detects Opsgenie alert pages
   - Pages refresh every 30 seconds while active
   - No manual intervention required

3. **Visual feedback**
   - Extension icon shows active status on supported pages
   - Console logs indicate refresh activity (visible in DevTools)

## 🌐 Supported URLs

The extension works on all Opsgenie alert-related pages:
- `https://*.app.opsgenie.com/alert/*`
- `https://*.opsgenie.com/alert/*`
- Alert lists, details, and dashboard pages

## 🛠️ Development

### Project Structure
```
opsgenie-auto-refresher/
├── manifest.json          # Extension configuration
├── background.js          # Service worker
├── content.js            # Page interaction script
├── icons/               # Extension icons
│   ├── icon16.png
│   ├── icon48.png
│   └── icon128.png
└── README.md
```

### Local Development
```bash
# Clone the repository
git clone https://github.com/yourusername/opsgenie-auto-refresher.git

# Make your changes
# Load extension in Chrome (see Manual Installation above)

# Test on Opsgenie pages
# Check browser console for debug information
```

### Building for Distribution
```bash
# Create distribution package
zip -r opsgenie-auto-refresher.zip . -x "*.git*" "*.md" "package*.json"
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Report bugs** - Open an issue with details and reproduction steps
2. **Suggest features** - Share ideas for improvements
3. **Submit pull requests** - Fix bugs or add new features
4. **Documentation** - Help improve this README or add code comments

### Development Guidelines
- Follow existing code style and structure
- Test thoroughly on multiple Opsgenie environments
- Update version numbers appropriately
- Add descriptive commit messages

## 📋 Changelog

### Version 0.0.2 (Current)
- ✅ Initial public release
- ✅ Auto-refresh functionality for Opsgenie alert pages
- ✅ Manifest V3 compatibility
- ✅ Chrome Web Store submission

## ❓ FAQ

**Q: Why every 30 seconds?**
A: This interval balances staying current with alerts while not overwhelming Opsgenie's servers.

**Q: Does this work with other incident management tools?**
A: Currently only Opsgenie is supported. Other tools may be added in future versions.

**Q: Will this affect my browser performance?**
A: No, the extension only runs on Opsgenie pages and uses minimal resources.

**Q: Is my data collected or tracked?**
A: No, this extension operates entirely locally and makes no external requests.

## 🐛 Known Issues

- Extension may need manual refresh if Opsgenie updates their page structure
- Some corporate firewalls may affect functionality
- Refresh timing may vary slightly based on browser performance

## 📧 Support

- **Issues**: [GitHub Issues](https://github.com/leoxtc/opsgenie-auto-refresher/issues)
- **Feature Requests**: [GitHub Discussions](https://github.com/leoxtc/opsgenie-auto-refresher/discussions)
- **Email**: your.email@example.com

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License - feel free to use, modify, and distribute
```

## 🙏 Acknowledgments

- Original project maintainer for the initial concept
- Opsgenie community for feature requests and feedback
- All contributors and users of this extension

---

<div align="center">

**Made with ❤️ for the DevOps community**

[⭐ Star this project](https://github.com/yourusername/opsgenie-auto-refresher) | [🐛 Report Issues](https://github.com/yourusername/opsgenie-auto-refresher/issues) | [💬 Discussions](https://github.com/yourusername/opsgenie-auto-refresher/discussions)

</div>