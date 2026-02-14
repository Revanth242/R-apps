# R-apps
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>App Repository Documentation</title>
    <style>
        body { font-family: sans-serif; line-height: 1.6; color: #333; max-width: 800px; margin: 40px auto; padding: 0 20px; }
        h1 { border-bottom: 2px solid #eee; padding-bottom: 10px; }
        h2 { color: #0056b3; margin-top: 30px; }
        code { background: #f4f4f4; border: 1px solid #ddd; padding: 2px 5px; border-radius: 3px; font-family: monospace; }
        pre { background: #f4f4f4; border: 1px solid #ddd; padding: 15px; overflow-x: auto; border-radius: 5px; }
        .feature-list { list-style-type: square; }
    </style>
</head>
<body>

    <h1>My App Name</h1>
    <p>A mobile application built with <strong>Kodular</strong> featuring an integrated QR/Barcode scanner and a custom <strong>GitHub-based OTA (Over-The-Air) update system</strong>.</p>

    <h2>🚀 Features</h2>
    <ul class="feature-list">
        <li><strong>Real-time Scanning</strong>: Efficiently scan and process data using the integrated scanner module.</li>
        <li><strong>Smart Update System</strong>: The app automatically checks this repository for a <code>version.json</code> file to ensure you are always running the latest version.</li>
        <li><strong>Forced Updates</strong>: A dedicated update overlay prevents app usage if a critical new version is available, ensuring security and compatibility.</li>
    </ul>

    <h2>📲 Installation</h2>
    <ol>
        <li>Download the latest <code>.apk</code> from the Releases section.</li>
        <li>Enable "Install from Unknown Sources" in your Android settings.</li>
        <li>Install the APK and launch the app.</li>
    </ol>

    <h2>🛠 How the Update System Works</h2>
    <p>The app performs a <code>GET</code> request to the raw URL of the <code>version.json</code> file in this repository. It compares the <code>version_code</code> in the JSON with the internal app version:</p>
    <ul>
        <li><strong>If JSON version &gt; App version</strong>: The update screen is triggered.</li>
        <li><strong>If JSON version &le; App version</strong>: The app continues to the main scanner interface.</li>
    </ul>

    <h2>📄 Versioning (version.json)</h2>
    <p>To push an update, the <code>version.json</code> file must be formatted as follows:</p>
    <pre>
{
  "version_code": 2,
  "download_url": "https://github.com/YourUsername/YourRepo/raw/main/app-release.apk"
}
    </pre>

</body>
</html>
