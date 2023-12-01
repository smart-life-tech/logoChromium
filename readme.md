

```markdown
# Raspberry Pi Splash Screen Setup

Welcome to the setup guide for creating a splash screen on your Raspberry Pi to display both a logo and an input field for entering a website URL.

## Prerequisites

- Raspberry Pi Model: Raspberry Pi 4 (4GB)
- Operating System: Raspberry Pi OS
- External HDMI Monitor
- DSI Touch Screen Monitor (800 x 480)
- Chromium Browser

## Step-by-Step Setup Guide

### 1. Clone the Repository

Clone this repository to your Raspberry Pi.

```bash
git clone https://github.com/smart-life-tech/logoChromium.git
cd your-repo
```

### 2. load the html page
### 3. Configure External Monitor

Connect your Raspberry Pi to an external HDMI monitor.

### 4. Configure DSI Touch Screen

Attach the DSI touch screen monitor.

### 5. Configure Display Cloning

Edit display settings to clone the DSI screen on the HDMI external monitor.

```bash
# Add specific commands for display configuration
```

### 6. Install Chromium Browser

Install Chromium on your Raspberry Pi.

```bash
sudo apt update
sudo apt install chromium-browser
```

### 7. Launch Chromium in Kiosk Mode
**modify the startup script**
```bash
nano /home/pi/start-chromium.sh
```
```bash
#!/bin/bash
unclutter -idle 0.1 -root &
chromium-browser --disable-infobars --kiosk --noerrdialogs --disable-session-crashed-bubble --disable-breakpad --disable-pinch --overscroll-history-navigation=0 --disable-features=TranslateUI --disable-software-rasterizer --disable-print-preview --disable-extensions --disable-restore-session-state --disable-sync --no-first-runweb.html
```

### 8. Test the Setup

Reboot your Raspberry Pi and check if the splash screen is displayed on both screens.

```bash
sudo reboot
```

## Additional Notes

- Include any additional notes or troubleshooting tips. message me

## Contributing

If you'd like to contribute to this project, please follow the [contributing guidelines](CONTRIBUTING.md).

## License

This project is licensed under the [MIT License](LICENSE).
```
