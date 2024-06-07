


# Day 1: Installation and Setup

Decided to work on Arduino IDE using Ubuntu OS to better familiarize myself with the OS and CLI.

## Step 1: Installing the IDE

1. Go to the Arduino main website and download the AppImage file.
2. Open Terminal and navigate to the Downloads folder using:
   ```bash
   cd ~/Downloads
   ```
3. Make the AppImage executable using `chmod`, which is a security function of Linux:
   ```bash
   chmod +x filename.AppImage
   ```
4. Run the AppImage:
   ```bash
   ./filename.AppImage
   ```

## Step 2: Adding the Shortcut to App Launcher

Use the following commands to install the app launcher:

```bash
sudo apt install software-properties-common
sudo add-apt-repository ppa:appimagelauncher-team/stable
sudo apt update
sudo apt install appimagelauncher
```

Now you can just run the AppImage file. It will launch the launcher app.

## Step 3 (Optional): Extract Pre-Installed Program (Fun Task)

I noticed that the board is already blinking (brand new Arduino board), so I thought about extracting the pre-installed program on the Arduino. This shall be done the next day (pre-installed program extraction).

## Knowledge

1. `chmod` = Security for Linux.
2. Two methods to install:
   - Install sh script (yet to be done)
   - AppImage (universal software package format)
3. PPA (?): This was used in the AppImage launcher repo addition.

## Additional Tasks

1. AppImage manual addition to launcher: try running the following commands for manual addition to the app launcher:
   ```
   [Desktop Entry]
   Type=Application
   Name=AppImage Name
   Exec=/path/to/squashfs-root/AppRun
   Icon=/path/to/squashfs-root/icon.png
   ```

### AI Help: To Create an App Launcher for an AppImage on Ubuntu, Follow These Steps:

1. **Extract the AppImage contents**:
   - Run the AppImage with the `--appimage-extract` option to extract its contents to a directory:
     ```bash
     ./appimage.AppImage --appimage-extract
     ```
   - This will create a `squashfs-root` directory containing the extracted files.

2. **Create a desktop entry file**:
   - Navigate to the `squashfs-root` directory and look for an executable file that launches the application.
   - Create a `.desktop` file in `~/.local/share/applications/` with the following contents:
     ```
     [Desktop Entry]
     Type=Application
     Name=AppImage Name
     Exec=/path/to/squashfs-root/AppRun
     Icon=/path/to/squashfs-root/icon.png
     ```
     Replace `AppImage Name` with the name of your application, `/path/to/squashfs-root/AppRun` with the actual path to the `AppRun` executable, and `/path/to/squashfs-root/icon.png` with the path to the application's icon file.

3. **Make the desktop entry file executable**:
   - Run:
     ```bash
     chmod +x ~/.local/share/applications/appimage.desktop
     ```
     to make the desktop entry file executable.

4. **Clean up**:
   - Remove the extracted `squashfs-root` directory to save disk space.

Now, your AppImage should be available in the application launcher and can be easily accessed from the Ubuntu sidebar or application menu.

This method creates a proper desktop integration for the AppImage, allowing it to be launched like any other installed application. It also ensures that the AppImage runs with the necessary permissions and dependencies.
```

This Markdown document should be well-structured and easy to read on GitHub, providing clear instructions and information about your Day 1 setup.
