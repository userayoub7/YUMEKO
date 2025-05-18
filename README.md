# PIKKA

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**PIKKA** is an open-source shell script designed for rooted Android devices, providing users with granular control over installed applications. Leveraging `su` root access, PIKKA facilitates the management of system and user-installed apps directly through the Android shell environment, prioritizing safe and deliberate operation.

---

## Table of Contents
- [Features](#features)
- [Technical Overview](#technical-overview)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

---

## Features

### Core Functionality
-   **Root Access (`su`)**: Execute commands with necessary elevated privileges to modify app states.
-   **App Freezing**: Disable applications to prevent them from running, without uninstalling them.
-   **App Removal**: Uninstall user and system applications. **Caution is strongly advised when removing system apps.**

### Safety Considerations
-   **Direct Execution**: Operations are performed via explicit shell commands issued by the user.
-   **Minimal Dependencies**: Relies primarily on the Android shell environment and root access.

### Basic Tools
-   **Command Output**: Script provides output of the underlying shell commands executed.
-   **Targeted Actions**: Allows specifying package names for precise management.

---

## Technical Overview

### Structure
-   **`pikka.sh`**: The main script file containing the logic for parsing arguments, handling root execution, and invoking Android's package manager (`pm`) commands.

### Dependencies
-   A rooted Android device with a functional `su` binary.
-   Standard Android shell utilities, notably the `pm` command.

---

## Getting Started

### Prerequisites
-   A rooted Android device running a compatible Android version.
-   Access to a terminal emulator on the device or ADB shell access from a computer.

### Installation
1.  **Clone the repository** (or download the script directly):
    ```bash
    git clone [https://github.com/yourusername/pikka.git](https://github.com/yourusername/pikka.git) # Replace with the actual repo URL
    ```
2.  **Transfer the script** (`pikka.sh`) to a convenient location on your Android device (e.g., `/data/local/tmp/`).
3.  **Grant execute permissions** to the script:
    ```bash
    chmod +x /path/to/pikka.sh
    ```
    *(Replace `/path/to/pikka.sh` with the actual path where you placed the script)*.

---

## Usage

1.  **Open a terminal** on your device or connect via `adb shell`.
2.  **Navigate to the script's directory**:
    ```bash
    cd /path/to/script
    ```
3.  **Execute the script with root privileges** using `su -c`, specifying the action and target package name(s).

    * **To remove an app**:
        ```bash
        su -c "./pikka.sh remove com.example.app"
        ```
        *(Replace `com.example.app` with the package name of the app you want to remove).*
        **WARNING**: Removing system apps can cause device instability or boot loops. Proceed with extreme caution.

    * **To freeze (disable) an app**:
        ```bash
        su -c "./pikka.sh freeze com.example.app"
        ```
        *(Replace `com.example.app` with the package name of the app you want to freeze).*

    * **To unfreeze (enable) an app**:
         ```bash
         su -c "./pikka.sh unfreeze com.example.app"
         ```
         *(Replace `com.example.app` with the package name of the app you want to unfreeze).*

    * Check script for other available commands or options.

---

## Contributing

We welcome contributions from the community! Feel free to submit issues for bug reports or feature requests, or open pull requests with improvements.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Support

If you find Pikka useful, please consider supporting the project:
-   ⭐ Star the repository on GitHub.
-   🛠️ Contribute code or report issues.
-   💬 Share feedback or suggestions.

---

Empower your rooted Android device with precise app control via the shell!
