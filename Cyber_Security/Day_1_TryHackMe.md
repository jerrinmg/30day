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
