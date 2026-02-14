# My App Name
A mobile application built with **Kodular** featuring an integrated QR/Barcode scanner and a custom **GitHub-based OTA (Over-The-Air) update system**.

### 🚀 Features
* **Real-time Scanning**: Efficiently scan and process data using the integrated scanner module.
* **Smart Update System**: The app automatically checks this repository for a `version.json` file to ensure you are always running the latest version.
* **Forced Updates**: A dedicated update overlay prevents app usage if a critical new version is available, ensuring security and compatibility.

### 📲 Installation
1. Download the latest `.apk` from the [Releases](#) section.
2. Enable "Install from Unknown Sources" in your Android settings.
3. Install the APK and launch the app.

### 🛠 How the Update System Works
The app performs a `GET` request to the raw URL of the `version.json` file in this repository. It compares the `version_code` in the JSON with the internal app version:
* **If `JSON version > App version`**: The update screen is triggered.
* **If `JSON version <= App version`**: The app continues to the main scanner interface.

### 📄 Versioning (version.json)
To push an update, the `version.json` file must be formatted as follows:
```json
{
  "version_code": 2,
  "download_url": "[https://github.com/YourUsername/YourRepo/raw/main/app-release.apk](https://github.com/YourUsername/YourRepo/raw/main/app-release.apk)"
}
