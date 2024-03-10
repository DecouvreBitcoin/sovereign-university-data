---
name: Tails

description: Install Tails on a USB key
---

![image](assets/cover.jpeg)

A portable and amnesic operating system that protects you against surveillance and censorship.

## Why have a USB key with Tails installed?

Tails (https://tails.boum.org/) is the easiest way to have a secure computer at your disposal at all times, which will not leave any trace on the computer you use it with.

To use Tails, turn off the computer you have access to (at your parents', at your friends', in an Internet café...) and start it with your Tails USB key instead of Windows, macOS, or Linux.

After that, you will have a workspace and communication environment that is independent of the usual operating system and never uses the hard drive.

Tails never writes to the hard drive and only uses the computer's RAM to function. This memory is completely erased when Tails is shut down, thus removing all possible traces.

## Some concrete use cases

To give you concrete ideas of the benefits of always having a USB key with Tails, here is a small non-exhaustive list compiled by the Agora256 team:

- Connect to the Internet and Tor in an uncensored and anonymous way to browse websites without leaving traces;
- Open a PDF from a suspicious website;
- Test your Bitcoin private key backup with the Electrum wallet;
- Use an office suite (LibreOffice) and work on a computer that does not belong to you;
- Take your first steps in a Linux environment to learn how to leave the world of Microsoft and Apple.

## How to trust Tails?

There is always an element of trust in using software, but it does not have to be blind. A tool like Tails must strive to provide its users with means to be trustworthy. For Tails, this means:

- Public source code: https://gitlab.tails.boum.org/;
- A project based on reputable projects: Tor and Debian;
- Verifiable and reproducible downloads;
- Recommendations by different individuals and organizations.

## Installation and usage guide

The purpose of this installation guide is to guide you through each step of the installation. We will not describe actions to be taken more than the official guide, but we will point you in the right direction while giving you tips and tricks.

For practical experience reasons, these tips will be focused on macOS and Linux platforms.
🛠️
Before starting this procedure, please make sure you have a USB key with a minimum read speed of 150 MB/s and a capacity of at least 8 GB, ideally USB 3.0.

Prerequisites:

- 1 USB key, only for Tails, with a capacity of at least 8 GB
- A computer connected to the Internet with Linux, macOS, (or Windows)
- Approximately one hour of free time, depending on your Internet connection speed, including ½ hour for installation (1.3 GB file to download)

## Step 1: Download Tails from your computer

![image](assets/1.webp)

> 🔗 Official Tails section: https://tails.boum.org/install/linux/index.fr.html#download

Downloading the installation file with the .img extension may take some time depending on your Internet download speed, so plan ahead. With a modern and efficient connection, it will take less than 5 minutes.

Save the file in a known folder, such as Downloads, as this will be necessary for the next step.

## Step 2: Verify your download

![image](assets/2.webp)

> 🔗 Official Tails section: https://tails.boum.org/install/linux/index.fr.html#verify

Verifying the download ensures that it is issued by the Tails developers and has not been corrupted or intercepted during the download.

It is possible to manually verify that the file you just downloaded is the expected one using PGP, but without advanced knowledge, this verification offers the same level of security as the JavaScript verification on the download page, while being much more complicated and prone to errors.

To verify the file, use the "Select your download..." button provided in the official section!

## Step 3: Install Tails on your USB key

![image](assets/3.webp)

> 🔗 Official Tails section:
>
> - Linux: https://tails.boum.org/install/linux/index.fr.html#install
> - macOS: https://tails.boum.org/install/mac/index.fr.html#etcher and https://tails.boum.org/install/mac/index.fr.html#install

This step of installing Tails on your USB key is the most difficult in the entire guide, especially if you have never done it before. The most important point is to choose the correct procedure in the official section for your operating system: Linux or macOS.

Once the tools are installed and prepared as recommended, the file with the .img extension can be copied to your key (erasing all existing data) to make it "bootable" independently.

Good luck! and see you at step 4.

## Step 4: Restart on your Tails USB key

![image](assets/4.webp)

> 🔗 Official Tails section: https://tails.boum.org/install/linux/index.en.html#restart
> It's time to start one of your computers using your new USB stick. Insert it into one of its USB ports and restart!

> 💡 Most computers do not automatically boot from the Tails USB stick, but you can press the boot menu key to display a list of possible devices to boot from.

To determine which key you should press to ensure that you have the boot menu allowing you to select the USB stick instead of your usual hard drive, here is a non-exhaustive list by manufacturer:

| Manufacturer | Key              |
| ------------ | ---------------- |
| Acer         | F12, F9, F2, Esc |
| Apple        | Option           |
| Asus         | Esc              |
| Clevo        | F7               |
| Dell         | F12              |
| Fujitsu      | F12, Esc         |
| HP           | F9               |
| Huawei       | F12              |
| Intel        | F10              |
| Lenovo       | F12              |
| MSI          | F11              |
| Samsung      | Esc, F12, F2     |
| Sony         | F11, Esc, F10    |
| Toshiba      | F12              |
| others...    | F12, Esc         |

Once the USB stick is selected, you should see this new boot screen, which is a very good sign, so let the computer continue to boot...

![image](assets/5.webp)

## Step 5: Welcome to Tails!

![image](assets/6.webp)

> 🔗 Official Tails section: https://tails.boum.org/install/linux/index.en.html#tails

One or two minutes after the boot loader and loading screen, the Welcome Screen appears.

![image](assets/7.webp)

In the Welcome Screen, select your language and keyboard layout in the Language & Region section. Click on Start Tails.

![image](assets/8.webp)

If your computer is not wired to your network, please refer to the official Tails instructions to help you connect to your network without Wi-Fi (section "Test your Wi-Fi").

Once connected to the local network, the Tor Connection wizard appears to help you connect to the Tor network.

![image](assets/9.webp)

You can start browsing anonymously, explore the options and software included in Tails. Enjoy yourself, you have plenty of room for errors, as nothing is modified on the USB stick... Your next restart will have forgotten all your experiences!

## In a future guide...

Once you have experimented a bit more with your own Tails USB stick, we will explore other more advanced topics in another article, such as:

> Update a key with the latest version of Tails; Configure and use persistent storage; Install additional software.
> Until then, as always, if you have any questions, feel free to share them with the Agora256 community. We are learning together to be better tomorrow than we are today!
