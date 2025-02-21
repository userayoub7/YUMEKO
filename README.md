# YUMEKO

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  
**YUMEKO** is a powerful, open-source Android app designed to give users full control over their devices by safely removing system and user-installed apps. Built with a focus on stability, security, and performance, YUMEKO leverages `su` root access and Shizuku integration to provide advanced app management capabilities.

---

## Table of Contents
- [Features](#features)
- [Technical Architecture](#technical-architecture)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

---

## Features

### Core Functionality
- **Root Access (`su`)**: Safely execute shell commands to remove or disable system apps.
- **Shizuku Integration**: Perform app management on non-rooted devices using Shizuku's API.
- **App Freezing**: Disable apps without uninstalling them.
- **System App Restoration**: Restore removed system apps from stock firmware.

### Safety and Stability
- **Automatic Backups**: Backup app data before removal using Room Database.
- **Dependency Checks**: Prevent system instability by validating app dependencies.
- **Undo Functionality**: Restore removed apps from backups with a single click.

### Advanced Tools
- **Logging and Recovery**: Detailed logs for troubleshooting and recovery options.
- **Custom Filters**: Identify and manage bloatware with predefined or custom filters.

---

## Technical Architecture

### Modules
1. **Core**:
   - Handles `su` and Shizuku integration.
   - Manages app removal, freezing, and restoration logic.
2. **UI**:
   - Provides a clean and responsive interface for app management.
3. **Utils**:
   - Backup and restore functionality using Room Database.
   - Dependency validation and logging tools.
4. **Models**:
   - Data classes for app information, backups, and logs.

### Dependencies
- **Shizuku API**: For non-rooted device support.
- **Room Database**: For backup and logging functionality.
- **Material Components**: For UI consistency (optional).

---

## Getting Started

### Prerequisites
- Android Studio (latest version).
- A rooted Android device or Shizuku-enabled device for testing.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/YUMEKO.git
   ```
2. Open the project in Android Studio.
3. Build and run the app on your device.

---

## Usage

1. **Grant Permissions**:
   - Grant root access or enable Shizuku when prompted.
2. **Manage Apps**:
   - Select apps to remove, freeze, or restore.
   - Use the undo functionality to restore removed apps if needed.
3. **Backup and Restore**:
   - Automatically backup app data before removal.
   - Restore apps from backups with a single click.

---

## Contributing

We welcome contributions from the community! Whether you're a developer, designer, or tester, your help is appreciated. Please read our [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to get started.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Support

If you find this project useful, consider supporting it by:
- ⭐ Starring the repository.
- 🛠️ Contributing code or reporting issues.
- 💬 Sharing feedback or suggestions.

---

Let’s build a safer, cleaner, and more efficient Android experience together! 🚀
