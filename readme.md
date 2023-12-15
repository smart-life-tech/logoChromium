
pkill -f chromium-browser

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

#enter this on the pi termial 

`sudo nano /etc/xdg/lxsession/LXDE-pi/autostart`
And add this to the last part :

```bash
@xset s off
@xset -dpms
@xset s noblank
@chromium-browser --kiosk /home/theavguys3/Downloads/logoChromium/web.html  # load chromium after boot and open the webs
```
save then exist, go to terminal 

`rebbot`

to do the wifi settings, when its not connected to the internet

here is the step i took to do mine.

in the kisok mode press the windows button fro your key board
select accesories-> terminal

Editing wpa_supplicant.conf directly
Open the wpa_supplicant.conf file for editing:

```bash
sudo nano /etc/wpa_supplicant/wpa_supplicant.conf
```
Add the following lines at the end of the file, replacing "your_SSID" and "your_password" with your Wi-Fi SSID and password:

```bash
network={
    ssid="your_SSID"
    psk="your_password"
}
```
Save the changes (Ctrl + X, then Y, then Enter).

Restart the Wi-Fi interface:

```bash
sudo ifdown wlan0
sudo ifup wlan0
```