# Pi Touch UI

This is a simple UI for a Raspberry Pi Touchscreen.

## Features

- Home Screen
- Settings Screen
- Info Screen

## Raspberry Pi Setup

### Install Raspbian

Since we have a Raspberry Pi 1 Model B, we need to install a 32 bit version of Raspbian. The most recent 32 bit version is Bookworm. Use the Raspberry Pi Imager to flash the OS to an SD card. We chose the Lite version.

Set any options as desired to change the default username/password and other settings, hostname, and WiFi settings. I also like to enable SSH with my public key.

### Update and Upgrade

Boot into your new Raspbian installation and run the following commands to update and upgrade:

```bash
sudo apt update && sudo apt -y full-upgrade
```

Reboot the Pi.

### Add WiFi Connections

Use the `nmtui` command to add your WiFi connections. This is a text based UI for [NetworkManager](https://forums.raspberrypi.com/viewtopic.php?t=357739).

```bash
sudo nmtui
```

### Install Python and Its Tooling

#### Install Python

```bash
sudo apt -y install python3-pip python3-venv
```

#### Create a Virtual Environment

```bash
python3 -m venv .venv --system-site-packages
source .venv/bin/activate
```

#### Install Python Pipenv

```bash
pip install pipenv
pipenv install
```

### Install Development Tools

```bash
sudo apt -y install git
```

### Set Up the Touchscreen

Use the tutorial at [Adafruit PiTFT - 2.8" Touchscreen Display for Raspberry Pi](https://learn.adafruit.com/adafruit-pitft-28-inch-resistive-touchscreen-display-raspberry-pi)
to install the touchscreen software and configure the display.

We have the Original PiTFT with the 2.8" display which uses the 2x13 pin connector of the original Raspberry Pi Model 1.

Follow the [Software Easy Install](https://learn.adafruit.com/adafruit-pitft-28-inch-resistive-touchscreen-display-raspberry-pi/easy-install-2) instructions.
