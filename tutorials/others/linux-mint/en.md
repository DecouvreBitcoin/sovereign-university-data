---
name: Linux Mint

description: Set up a computer for bitcoin transactions
---

![image](assets/cover.jpeg)

## What’s wrong if you use a regular computer?

When making Bitcoin transactions, it’s ideal if your computer has no malware. Obviously.

If you keep your Bitcoin seed phrase (usually 12 or 24 words) off the computer with a signing device (eg a hardware wallet – its main purpose), then you might think it’s not that important to have a “clean” computer – not true.

A malware-infested computer may read your Bitcoin addresses, exposing your balance to an attacker – they can’t take bitcoin just from knowing the address, but they can see how much you have, and calculate from that if you are a worthy target. They may also somehow work out where you live, for example, and extract fingernails or children from you to get you to pay a ransom.

## What is the solution?

I encourage most Bitcoiners to use a dedicated malware-free computer (with internet access) for making Bitcoin transactions. I suggest people use an open-source operating system like Linux Mint, but use Windows or Mac if you must – that’s better than using a regular, well-used computer that invariably has malware hidden in it.

One obstacle that people come across is installing a new operating system on such computers. This guide is to help with that.

There are many varieties of Linux and I have tried several. My recommendation for Bitcoiners is Linux Mint, because it is easy to install, very fast (particularly on bootup and shutdown), not bloated (every extra piece of software is a risk), and has rarely crashed on me or behaved weirdly (compared to other versions like Ubuntu and Debian).

Some may be very resistant to a new operating system, preferring Windows or Mac OS. I understand, but the Windows and Apple operating systems are closed source, so we have to trust what they’re doing; I don’t think that’s a good policy, but it’s not all-or-nothing. I’d much prefer people use a dedicated freshly installed Windows or Mac OS computer rather than a well-used computer (with who knows what malware has accumulated on it). One step better is to use a freshly installed Linux computer, which is what I’ll be demonstrating.

If you’re nervous about using Linux because of the unknown, that’s natural, but so is spending some time to learn. So much information is available online. Here is an excellent short video introducing the basics of the command line that I highly recommend.
Choose a computer

I’ll start with what I think is the best option. Then I’ll give my opinion on alternatives.

Ideal option:

My recommendation, if you can afford it, and if the size of your bitcoin stack justifies it, is to get a brand new entry-level laptop. The most basic model built these days is good enough to handle what it’s going to be used for. The processor and RAM specs are not relevant, because they will all be good enough.

Avoid:

- Any tablet combo, including Surface Pro
- Chromebooks – often the storage capacity is too low
- Any computer with an eMMC drive; If it has an SSD drive, that’s perfect
- Macs – they are expensive, and the hardware doesn’t gel well with Linux operating systems in my experience
- Anything refurbished or 2nd hand (not an absolute deal-breaker though)

Instead, look for a Windows 11 laptop (Currently Windows 11 is the latest release. We’ll be getting rid of that software, don’t worry.). I searched on amazon.com for “Windows 11 Laptop” and found this good example:

![image](assets/1.webp)

The price of this one above is good. The specs are good enough. It has a build-in camera which we can use for QR code PSBT transactions (otherwise you’d have to buy a USB camera to do that). Don’t worry about the fact that it’s not a well-recognised brand (it’s cheap). If you want a better brand, it’ll cost you, eg:

![image](assets/2.webp)

Some of the cheaper ones have only 64Gb of drive space; I haven’t tested laptops with drives that small – it probably is OK to have 64Gb, but it might be pushing it.

## Other options – Tails

Tails is an operating system that boots from a USB thumb drive, and temporarily takes over the hardware of any computer. It uses Tor connections only, so you’d need to be comfortable using Tor. None of the data that you write to memory during your session is saved to the drive (it starts fresh every time) unless you tweak the settings and create a permanent storage option (on the USB thumb drive) – which you lock with a password.

It’s not a bad option and it’s free, but it’s a little clunky for our purpose. Installing new software on it is not a breeze. One good feature is that it comes with Electrum, but the downside of this is that you didn’t install it yourself. Make sure the USB drive you use is at least 8Gb.

Your flexibility is reduced if you use Tails. You may not be able to follow various guides to set up what you need and get it working properly. For example, if you follow my guide to installing Bitcoin Core, there are modifications needed to make it work. I don’t think I’ll be making a Tails specific guide, so you’d need to build your skills and do it alone.

I also am not sure how well hardware wallets will interact with this OS.

Having said all this, a Tails computer for Bitcoin transactions is a nice additional option, and will certainly help your overall privacy skills to learn to use Tails.

## Other options – Live OS Boot

This is very similar to Tails, except the operating system is not privacy-dedicated. The basic way to use this is to flash a USB drive with the Linux operating system of your choice and make the computer boot from that instead of the internal drive. How to do this is explained later.

The advantage is that you are less restricted and things will work without advanced tweaks.

I am not sure how well such a system isolates malware on the existing computer from the USB boot drive you use that holds the new operating system. It probably does a fine job and is probably not as good as Tails. Because I don’t know, my preference is the dedicated laptop.
Other options – Your own used laptop or desktop computer

Using a used computer is not ideal, mainly because I am unaware of the inner workings of sophisticated malware, nor if wiping a drive is sufficient to get rid of it. It probably is but I don’t want to underestimate how clever nefarious hackers can be. You can decide, I don’t want to commit.

If you choose to use an old desktop instead of an old laptop, this will be fine, except that it will permanently take up space for your probably-rare bitcoin transactions; you shouldn’t be using it for anything else. Whereas with a laptop, you can just put it away, and even hide it for extra security.

## Installing Linux Mint on any computer

These are instructions to wipe any operating system from your new laptop and install Linux Mint, but you can adapt it to install just about any Linux version on just about any computer.

We are going to use any computer to flash the operating system to a memory stick of some sort. It doesn’t matter which memory stick, as long as it is compatible with a USB port, and I suggest 16Gb minimum.

Get one of these things:

![image](assets/3.webp)

Or you can use something like this:

![image](assets/4.webp)

Next, navigate to linuxmint.com

![image](assets/5.webp)

Hover the mouse over the Download menu at the top and then click the link, “Linux Mint 20.3” or whatever version is the latest recommended one at the time you do this.

![image](assets/6.webp)

There will be a few “flavours” to choose from. Go with “Cinnamon” to follow along with this guide. Click the Download button.

![image](assets/7.webp)

On the next page, you can scroll down to see the mirrors (Mirrors are various servers that hold a copy of the file we want). You can verify the download using SHA256 and gpg (recommended), but I’m going to skip explaining that here as I have written guides on this already.

![image](assets/8.webp)

Choose a mirror that’s closest to you and click its link (the green text in the mirror column). The file will begin downloading – the version I’m downloading is 2.1 gigabytes.

Once it’s downloaded, you can flash the file to a portable memory device and make it bootable. To do this, the easiest way is to use Balena Etcher. Download and install it if you don’t have it.

Then run it:

![image](assets/9.webp)

Click flash from file, and select the LinuxMint file you downloaded.

Then click Select target. Make sure the memory device is plugged in and make sure you are selecting the correct drive, otherwise you may destroy the contents of the wrong drive!

After that, select Flash! You may need to enter your password. When it’s completed, the drive is likely not going to be readable by your Windows or Mac computer because it has been transformed into a Linux device. Just pull it out.
Preparing the target computer

Turn on the new laptop, and while it is powering up, hold down the BIOS key. This is typically F2, but it could be F1, F8, F10, F11, F12 or Delete. Try each one until you get it, or search the internet for your computer’s model and ask the right question.

Eg “BIOS key Dell laptops”.

Every computer will have a different BIOS menu. Explore and find which menu allows you to configure the boot order. For our purposes, we want the computer to try to boot from a USB connected device (if there is one connected), before trying to boot from the internal hard drive (otherwise Windows will load). Once you set that, you may need to save before exiting or it may save automatically.

Reboot the computer and it should load from the USB memory device. We can not install Linux on the internal drive and Windows will be removed for good.

When you get to the following screen, select “OEM install (for manufacturers)”. If you instead choose “Start Linux Mint”, you’ll get a Linux Mint session loaded off the memory device, but once you shut down the computer, none of your information is saved – it’s basically a temporary session so you can try it out.

![image](assets/10.webp)

You will be taken through a graphical wizard which will ask you a number of questions that should be straightforward. One will be Languange settings, another will be your home internet network connection and password. If prompted to install additional software, reject it. When you get to the question about the installation type, some people may hesitate – you need to choose “Erase disk and install Linux Mint”. Also, do not encrypt the drive and do not select LVM.

You will eventually get to the desktop. At this point, you are not quite finished. You are actually acting as the manufacturer (i.e. someone building a computer and setting up Linux for the customer). You need to double click the desktop icon, “Install Linux Mint”, to finalise it.

![image](assets/11.webp)

Remember to remove the memory stick, and then reboot. After reboot, you’ll be using the operating system for the first time as a new user. Congratulations.

One of the first things to do (and to do regularly), is to keep the system up to date.

Open the Terminal application, and type the following:

```bash
sudo apt-get update
```

hit <enter>, confirm your choice, and then this command:

```bash
sudo apt-get upgrade
```

hit <enter> and confirm your choice.

Let it do its thing, it could take several minutes.

Next, I like to install Tor (case sensitive):

```bash
sudo apt-get install tor
```

> _ADDITION: You can also run the Linux Mint boot from “OEM install” (Make sure you are connected to the internet, otherwise you could get errors). If you do this, you later need to click the “ship to end user” icon which should be on the desktop. You then reboot and start the operating system as though you are opening the computer for the first time._

This guide explained why you may need a dedicated computer for Bitcoin transactions, and how to install a fresh Linux Mint operating system on it.
