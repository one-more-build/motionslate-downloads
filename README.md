# MotionSlate Blender Extension

Official downloads repository and extension feed for the **MotionSlate** Blender extension.

- **Extension Feed URL**: `https://one-more-build.github.io/motionslate-downloads/index.json`
- **Supported Blender Version**: Blender 5.2.0 LTS (or compatible 5.2.x builds)
- **Supported Platform**: macOS on Apple Silicon (`macos-arm64`)

---

## Installation Guide

### Method 1: Add Extension Repository in Blender (Recommended)

Adding the repository feed allows Blender to automatically discover new releases, notify you of updates, and install or upgrade MotionSlate directly from the Blender UI.

1. Open **Blender 5.2 LTS**.
2. Go to **Edit → Preferences → Get Extensions**.
3. In the top-right corner of the Preferences window, click the menu button (three horizontal lines or repository icon) and choose **Repositories**.
4. Click **+ Add Repository**.
5. Fill in the repository details:
   - **Name**: `MotionSlate`
   - **Custom URL**: `https://one-more-build.github.io/motionslate-downloads/index.json`
6. Click **Save & Sync**.
7. Return to the **Get Extensions** tab, search for **MotionSlate**, and click **Install**.
8. Once installed, ensure the extension is enabled. The MotionSlate panel will appear in the 3D Viewport sidebar (press `N` in the 3D Viewport).

---

### Method 2: Manual Installation from `.zip` Archive

If you prefer to download and install the standalone package directly:

1. Download the latest release package:
   - [`motionslate-0.3.0.zip`](./motionslate-0.3.0.zip)
   - SHA-256 Checksum: [`motionslate-0.3.0.zip.sha256`](./motionslate-0.3.0.zip.sha256)
2. *(Optional)* Verify the archive integrity in your terminal:
   ```sh
   shasum -a 256 -c motionslate-0.3.0.zip.sha256
   ```
3. Open **Blender 5.2 LTS**.
4. Go to **Edit → Preferences → Get Extensions**.
5. In the top-right corner, click the drop-down menu and choose **Install from Disk...**.
6. Select the downloaded `motionslate-0.3.0.zip` file.
7. Blender will install and activate the extension automatically.

---

## Upgrades

- **Via Repository Feed**: When a new version is published, an **Update** button appears next to MotionSlate in **Edit → Preferences → Get Extensions**. Click **Update** to apply the update seamlessly.
- **Via Disk**: Download the new `.zip` archive and choose **Install from Disk...**. Blender will replace the previous version cleanly.

---

## Permissions and Security

Blender 5.2 requires extensions to declare system permissions in their manifest:

- **Network (`127.0.0.1`)**: Used exclusively to communicate over local loopback with the MotionSlate recorder service. No external internet traffic is generated.
- **Files**: Used to read character joint-to-bone mapping profiles (JSON) and access motion journals in your selected capture directory.

No telemetry, tracking, or external cloud services are used.
