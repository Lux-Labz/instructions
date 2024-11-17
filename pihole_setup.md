# Pi-hole Server Setup Guide

Welcome to the **Pi-hole Server Setup Guide**! This step-by-step guide will help you block ads and enhance your network security. Follow along, and soon you'll have your Pi-hole server up and running smoothly. Let's get started!

## Table of Contents
- [Introduction](#introduction)
- [What You'll Need](#what-youll-need)
- [Step 1: Prepare the Hardware](#step-1-prepare-the-hardware)
- [Step 2: Install Raspbian OS](#step-2-install-raspbian-os)
- [Step 3: Install Pi-hole](#step-3-install-pi-hole)
- [Step 4: Configure Your Router](#step-4-configure-your-router)
- [Step 5: Access Pi-hole Dashboard](#step-5-access-pi-hole-dashboard)
- [Step 6: Update and Maintain](#step-6-update-and-maintain)
- [Conclusion](#conclusion)

---

## Introduction

Pi-hole is a network-wide ad blocker that helps you filter out unwanted ads at the network level. This guide will show you how to install Pi-hole on a Raspberry Pi, but you can also install it on any Linux server. It’s a great way to enhance your browsing experience and improve your home network security.

## What You'll Need

Before we dive into the steps, make sure you have the following:
- A **Raspberry Pi** (or another Linux server)
- A **microSD card** (at least 8GB)
- **Raspbian OS** installed on your microSD card
- **Keyboard**, **mouse**, and **monitor** for the initial setup
- **Ethernet cable** (optional but recommended for a stable connection)
- **Power supply** for your Raspberry Pi
- Internet connection

---

## Step 1: Prepare the Hardware

1. Insert the **microSD card** into your Raspberry Pi.
2. Connect your **keyboard**, **mouse**, and **monitor** to the Raspberry Pi.
3. Plug in the **Ethernet cable** (if using a wired connection).
4. Power up your Raspberry Pi with the **power supply**.

Great! Your Raspberry Pi should now boot up with the Raspbian OS.

---

## Step 2: Install Raspbian OS

If you haven't already installed Raspbian OS:
1. [Download Raspbian](https://www.raspberrypi.com/software/) and flash it to your microSD card using a tool like **balenaEtcher**.
2. Insert the microSD card and boot up your Raspberry Pi.
3. Follow the on-screen prompts to complete the Raspbian setup.

You're doing awesome! Now let's move on to installing Pi-hole.

---

## Step 3: Install Pi-hole

1. Open the terminal on your Raspberry Pi.
2. Run the following command to install Pi-hole:
    ```bash
    curl -sSL https://install.pi-hole.net | bash
    ```
3. Follow the installation prompts. You’ll be asked to:
    - Choose your network interface (eth0 for Ethernet, wlan0 for Wi-Fi).
    - Select an upstream DNS provider (like Google, OpenDNS, etc.).
    - Choose to block ads over IPv4 or IPv6 (IPv4 is generally enough).
    - Confirm the web admin interface installation.

Perfect! Pi-hole is now installed and ready to block those ads.

---

## Step 4: Configure Your Router

Now let's configure your router to send all DNS traffic through Pi-hole.

1. Log into your **router's settings** (usually found at 192.168.1.1 or 192.168.0.1).
2. Find the **DNS settings** (usually under LAN or DHCP settings).
3. Set the **DNS server** to your Raspberry Pi’s IP address (you can find this using the `hostname -I` command on your Pi).

Awesome! Your Pi-hole server is now blocking ads for all devices on your network.

---

## Step 5: Access Pi-hole Dashboard

1. Open your browser and type in your Pi-hole's IP address followed by `/admin` (e.g., `http://192.168.1.100/admin`).
2. Log in using the password provided during installation.
3. From here, you can monitor your network activity, adjust settings, and much more!

Well done! You now have full control over your network’s ad-blocking features.

---

## Step 6: Update and Maintain

To keep your Pi-hole running smoothly, make sure you update it regularly:
1. Open the terminal and run:
    ```bash
    pihole -up
    ```
2. You can also add or remove blocklists from the admin interface for more precise ad blocking.

Keep up the great work!

---

## Conclusion

Congratulations! You’ve successfully set up your very own Pi-hole server. Say goodbye to annoying ads and trackers and enjoy a cleaner, faster browsing experience. Don’t forget to keep your Pi-hole updated for the best performance.

If you have any questions or run into issues, feel free to reach out to the community or check out [Pi-hole’s documentation](https://docs.pi-hole.net/).

Happy ad-blocking! 😊
