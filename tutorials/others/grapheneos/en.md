---
name: GrapheneOS

description: Graphene OS tutorial
---

> "[GrapheneOS](https://grapheneos.org/) is a privacy and security focused mobile OS with Android app compatibility developed as a non-profit open source project."

GrapheneOS, originally founded in 2014 as 'CopperheadOS' is based on the traditional Android Code (AOSP), but with many changes and improvements aimed at improving user privacy and security. GrapheneOS puts the user in control of their phone, not the big tech companies.

### Sommaire:

- Intro
- Preparation
- Install
- App Alternatives
- Downsides
- Useful Info

Guide by https://github.com/BitcoinQnA/Bitcoiner.Guide/blob/main/grapheneos.md

## Why use GrapheneOS?

Modern phones are $500-$1000 tracking and data harvesting devices. Every single facet of our life runs through them, and unfortunately much of this data is shared with third parties in some form or another.
GrapheneOS is built specifically to reduce this data sharing and improve your device security from potential attack vectors. There's no such thing as a GrapheneOS account. You don't need one to download apps or interact with the OS. Simply put, you are not the product.

GrapheneOS provides additional security to your Android experience through some simple core principles.

1. **Attack surface reduction** - Remove unnecessary code (or bloatware).
2. **Vulnerability exposure prevention** - Allow the user enough granularity to choose the compromises they're comfortable with.
3. **Sandbox containment** - GrapheneOS fortifies existing Android sandboxes, further locking down each app's ability to communicate with the rest of your phone.

Learn more about the technical details of the GrapheneOS feature set [here](https://grapheneos.org/features).

### Easing the Transition

If you've been entrenched within the Google or Apple ecosystem for years, the thought of losing all that convenience overnight can be a scary one. But with some carefully considered app install decisions (covered later), much of this expected difficulty can be reduced or removed.

As good as the alternatives are becoming, the thought of such a change can still be off-putting. If you find yourself in this situation, my best advice is to run your new GrapheneOS device alongside your existing phone for a while. From there you can slowly wean yourself off 2-3 apps per week until you find yourself only reaching for your GrapheneOS device.

If you take this approach, be strict with yourself and cut off your reliance on the surveilled alternatives as quickly as possible. Us humans are lazy and will often take the path of least resistance. Remember why you made the switch in the first place.

**Instead of paying with your personal data, you chose to pay with your time, and sometimes your hard earned money (depending on the alternative apps you install).**

## Getting Started

GrapheneOS is currently only in production for _(rather ironically)_ the [Google Pixel](https://grapheneos.org/faq#supported-devices) range of phones. This does not come without good reason though. Pixel's offer the best hardware-based security to complement the work done to harden the OS. This includes things like specific component isolations and verified boot.

### Choosing a device

When choosing the Pixel you want to install GrapheneOS on, ensure you check how long the device will continue getting default [security updates](https://support.google.com/pixelphone/answer/4457705?hl=en#zippy=%2Cpixel-xl-a-a-g-a-g) for.

At the time of writing, the Pixel 6a is the cheapest model available with good long term support, guaranteed until July 2027. If you do choose this model, OEM unlocking won't work with the version of the stock OS from the factory. You need to update it to the June 2022 release or later via an over-the-air update. After you've updated it you'll also need to factory reset the device to fix OEM unlocking. All other models that are carrier unlocked will be ready for GrapheneOS straight out of the box.

When choosing a device you'll also want to ensure you purchase an unlocked version. Certain carriers like Verizon ship their units that are bootloader locked which completely prevents the following process.

### Installing GrapheneOS

The GrapheneOS [web installer](https://grapheneos.org/install/web) makes the entire process a breeze, and one that can be completed by anyone in under 10 minutes.
The following instructions are a cut down version taken from the link above.

All you need to hand is:

- The Pixel
- A USB cable to go from the phone to your computer
- A computer to run a web browser (any Chromium-based browser: Chrome, Edge, Brave, etc.)

1. The first step is to go to **Settings** > **About phone** and repeatedly tap the build number until you see **'Developer Mode'** is activated.
2. Next head to **Settings** > **System** > **Developer Options** and enable **'OEM Unlocking'**.
3. Now reboot the device and hold the volume down button whilst the phone is turning back on.
4. Connect the phone to your laptop and if prompted for authorization, allow the connection.
5. On the web installer page, click on 'Unlock the bootloader'.
6. You'll then see the phone options change. Use the volume button to change the selection to `unlock` and use the power button to accept.
7. Next click download release on the web installer page.
8. Once fully downloaded, move on to the next step and click 'Flash release'. This will take a minute or two and you do not need to touch the phone at all.
9. Finally, move to the next step of the web installer and click **Lock Bootloader**. You'll need to change the selection and confirm with the power button in the same way you did earlier in the process.
10. When you see the word `Start`, confirm this with the power button and the device will boot into your new Google-free operating system.

![image](assets/2.webp)

GrapheneOS start screen


_After initial boot and setup, it is good practice to disable OEM unlocking from Settings > System > Developer Options._

_You may also want to take the extra, optional but recommended step of verifying the install via the Auditor app. You'll need a separate Android phone with the app installed to complete this step. Instructions for this can be found [here](https://attestation.app/tutorial)._


![video](https://www.youtube.com/embed/L1KZWjZVnAw)

Video detailing the simple steps outlined above


If those simple steps seem like a step too far, you could consider purchasing a Pixel with the GrapheneOS software [pre-installed](https://ronindojo.io/en/roninmobile). Just be aware that you're putting a small amount of trust into the provider.

### Pre Installed Apps

Now that you're set up, you might notice how bare bones GrapheneOS appears upon first installation. By default you'll have these apps installed:

![image](assets/3.webp)

Default apps


The only two you may not be familiar with are 'Auditor' and 'Vanadium'.

- 'The [Auditor app](https://play.google.com/store/apps/details?id=app.attestation.auditor) uses hardware-based security features to validate the identity of a device along with authenticity and integrity of the operating system. It will verify that the device is running the stock operating system with the bootloader locked and that no tampering with the operating system has occurred.'
- [Vanadium](https://github.com/GrapheneOS/Vanadium) is a privacy and security hardened variant of Chromium web browser.

## Customization

Phone settings are a personal thing, but here are some of the first items I change when installing GrapheneOS to make myself feel more at home.

### Setting a wallpaper and updating the theme

Head to Settings > Wallpaper and Style. From here I:

- Update the home and lock screen backgrounds for images downloaded from the web.
- Choosing the accent colors used throughout the UI.
- Enable Dark theme.

### Show battery percentage

Head to **Settings** > **Battery**, then enable **Show battery percentage** in the status bar.

### Import contacts

**From another Android phone** - Head to Contacts app and look for the Export to VCF option.

**From iOS** - Use an app like Export Contact and use the 'vCard' export option to export a VCF file.
Once you have the VCF file, you can transfer across to your GrapheneOS device with an external storage option like microSD card or USB drive. If you don't have any of those to hand, you could opt to share via one of the many apps listed below.

![image](assets/4.webp)

Personalized home screen


## Alternative Apps

To make your phone useful you're going to want to install some applications! The options that follow are included because I have used them all personally or because they receive strong recommendations from the wider privacy community. There are many other great alternatives available that aren't mentioned, and [Awesome Privacy](https://awesome-privacy.xyz) offers an incredibly extensive list of privacy preserving applications for all types of device.

Just because an app is Free and Open Source Software (FOSS) does not mean it is free from potential privacy leaks. Use [Exodus](https://reports.exodus-privacy.eu.org/en/) to see how your preferred apps perform against their privacy audits.

### F-Droid

[F-Droid](https://f-droid.org/) is an installable catalogue of FOSS applications for Android. The client makes it easy to browse, install and update applications on your device. It's worth mentioning that updates via F-Droid can sometimes be slower than with other app stores. This is mainly dependent on whether or not the app is found via the main F-Droid repository or a custom one.

To install F-Droid simply head to their website via a browser on your GrapheneOS phone and tap download. This will download an `.apk` file. You'll then be asked if you'd like to install the app.

As well as applications found within the default repository in F-Droid, many Open Source projects will also host their own repository that can be added in the F-Droid app settings. If this is the case, the project in question will walk you through the very simple steps required to achieve this on their website.

![image](assets/5.webp)

F-Droid home screen

### Aurora Store

[Aurora Store](https://auroraoss.com/) is a FOSS version of the Google Play store. Aurora looks and feels very similar to the traditional Play Store and allows you to download and update any app you'd normally find via the Google option.

The killer feature of Aurora is anonymous log in. This means you can download any of your favorite apps that aren't available via F-Droid or direct APK, without having to be logged into your Google account.

Before you rush to make this your default install option, remember that many of the applications we're trying to get away from were installed from the Play Store. Just because they're accessible from Aurora doesn't change the fact that some may have tracking features embedded. It won't always be possible, but whenever you can, look for an F-Droid alternative before downloading via Aurora.

To install Aurora, simply search 'Aurora Store' in F-Droid.

Aurora does also have some potential attack vectors, as the "anonymous accounts" are really created and controlled by Aurora. They could, in theory, serve malicious updates or push apps to your phone, though you'd still have to accept the install prompt on device. Aurora also sometimes has some issues with apps not showing up due to region and device misreadings. This can usually be worked around with the steps below.

**Top tip** - Sometimes the Aurora Store will experience rate limiting which limits your ability to search and install apps. To get around this go to **Settings** > **Apps** > **Aurora** > **Open by default**, then add the domain `play.google.com`. Now, whenever navigate to a product or service's website that has the 'Download via Play Store' link, tapping on it will open that app within Aurora for you to download.


![image](assets/6.webp)

Aurora Store home screen

### APK Download

Apps on Android can also be downloaded and installed via an `.apk` file. This is a great alternative that requires zero third party app stores, simply download the file directly from the project or services' website or GitHub repository.

The downside to this approach is that you don't get automatic updates, so you'll need to monitor that service's communication channels to learn about new releases. However there is a a great project called Obtanium that aims to fix this. [Obtainium](https://github.com/ImranR98/Obtainium) allows you to install and update Open-Source apps directly from their releases pages, and receive notifications when new releases are made available.

![image](assets/7.webp)

Obtanium preview

### Web Apps

For times where you might want to infrequently use a service and do not want to download a native application, you can simple access the web version. Many websites nowadays also offer Progressive Web App (PWA) support. This is where you can bookmark a specific website (eg Twitter.com) to your phone's home screen. Then when you tap on the icon it opens as a full screen application without the usual distractions that come with the typical browser experience. You can see an example of how this looks below.

To achieve this in Vanadium, GrapheneOS' native browser, simply navigate to the website of choice, tap the three vertical dots in the top right corner of the screen and then tap **'Add to Home Screen'**.

The only downside of this approach is that because this is just a bookmarked web page, you won't get any form of notifications. Though some might see that as a positive!

![image](assets/8.webp)

Twitter PWA

### Web Browsers

You can't really go wrong with the pre-packaged option, Vanadium. The app behaves identically to any other mobile browser I've tried and I've not once had any compatibility issues.

For times when you need to access Tor native `.onion` sites, you can download the Tor Browser APK directly from their [website](https://www.torproject.org/download/#android) or via F-Droid.

### VPNs

To protect your online activity from your snooping internet service provider (ISP), a Virtual Private Network (VPN) app is a good option. A VPN sends your internet traffic in an encrypted tunnel to a shared IP address controlled by the VPN service provider to ensure your device activity cannot be linked to you.

The following are 3 well respected options that allow you to pay for the service in Bitcoin and without providing any personal information. All 3 options are available via F-Droid.

- [Mullvad](https://f-droid.org/packages/net.mullvad.mullvadvpn/)
- [Proton](https://f-droid.org/en/packages/ch.protonvpn.android/)
- [iVPN](https://f-droid.org/en/packages/net.ivpn.client/)

### Messaging

In recent years encrypted messaging solutions have become plentiful. The problem remains though, you can have the best and most private option installed on your phone, but if you have no contacts that use it, what's the point?

Most people who have no interest in the privacy space are likely to be using WhatsApp or iMessage. The former can be downloaded via the Aurora Store but the latter is not going to work on GrapheneOS (obviously!).

- [Signal](https://signal.org/) is one of the more popular end-to-end encrypted (E2EE) messengers that has a strong track record and rich feature set. Signal requires a phone number for sign up, so if you plan on chatting with people that you'd rather did not know your phone number, perhaps look into some of the alternatives. Signal must be downloaded via the Aurora Store.
- [Simplex](https://f-droid.org/en/packages/chat.simplex.app/) is a fairly new E2EE messenger. It has no user ID, requires no phone number or personal information. People find you by scanning your personal QR code or by visitng your unique link. Simplex also allows advanced users to run their own server to further reduce reliance on any centralized entity. Simplex does not have a desktop client, so may not be suitable if multi-device is on your priority list. Simplex for Android is available via F-Droid.
- [Threema](https://threema.ch/en/faq/libre_installation) offers a similar experience to Simplex, but has been around for longer and as a result, feels a little more polished. Threema is not free, a lifetime license costs $4.99 and can be bought with Bitcoin. Threema offers a web client and native desktop applications. The Android application is available via F-Droid.
- [Telegram FOSS](https://f-droid.org/en/packages/org.telegram.messenger/) is an unofficial FOSS fork of the official Telegram app for Android. Telegram has E2EE 'secret chats', but the default option is not private. Telegram FOSS can be downloaded from F-Droid.

![image](assets/9.webp)
Left: Threema
Right: Simplex

### Media

- [Spotube](https://f-droid.org/packages/oss.krtirtho.spotube/) is a cross-platform Spotify client that doesn't require a Premium account. Spotube is available via F-Droid.
- [ViMusic](https://f-droid.org/en/packages/it.vfsfitvnm.vimusic/) is a fantastic application for steaming any music from YouTube music, for free. ViMusic is available from F-Droid.
- [Newpipe](https://f-droid.org/packages/org.schabi.newpipe/) offers a YouTube experience without the annoying adverts and questionable permissions. With NewPipe you can subscribe to channels, listen in the background and even download for offline viewing. NewPipe is accessible via F-Droid.
- [AntennaPod](https://f-droid.org/packages/de.danoeh.antennapod/) is a podcast player that allows you to subscribe and manage all of your favorite shows. AntennaPod is available via F-Droid.

![image](assets/11.webp)

Left: Spotube
Right: ViMusic

### Maps

If you want voice assistance whilst driving and using a maps app in GrapheneOS, you'll need to install [RHVoice](https://rhvoice.org/installation/) and [configure](https://discuss.grapheneos.org/d/2488-organic-maps-app-voice-instructions-are-not-available) it.

- [Magic Earth](https://www.magicearth.com/) is a maps alternative that supports turn-by-turn navigation, 3D and offline maps. Magic Earth can be downloaded from the Aurora Store.
- [Organic Maps](https://f-droid.org/en/packages/app.organicmaps/) is maps alternative for travelers, tourists, hikers, and cyclists based on top of crowd-sourced OpenStreetMap data. It is a privacy-focused, open-source fork of Maps.me app (previously known as MapsWithMe). It supports 100% of features without an active Internet connection and can be downloaded from F-Droid.
- [OsmAnd](https://f-droid.org/en/packages/net.osmand.plus/) is another great maps alternative that supports all of the features mentioned above.

![image](assets/13.webp)

Left: Magic Earth
Right: Organic Maps

### Email

- [Proton Mail](https://proton.me/mail) offers a free private email service that supports audited E2EE. Proton also offers a paid version that supports custom domains and [aliasing](https://proton.me/support/creating-aliases). Proton Mail can be downloaded as a direct APK or via Aurora.
- [Tutanota](https://tutanota.com/) offers the same features as Proton Mail, including optional paid services and can be downloaded as a direct APK or via F-Droid.
- [K-9 Mail](https://f-droid.org/en/packages/com.fsck.k9/) is an open source email client that works with basically every email provider. It supports multiple accounts, a unified inbox and the OpenPGP encryption standard.

![image](assets/15.webp)

Left: Proton Mail
Right: Tutanota

### Productivity

- [Syncthing](https://f-droid.org/packages/com.nutomic.syncthingandroid/) is a file synchronization program. It synchronizes files between two or more devices in real time, safely protected from prying eyes. Your data is your data alone and you deserve to choose where it is stored, whether it is shared with some third party, and how it’s transmitted over the internet. Syncthing is available via F-Droid.
- [KDE Connect](https://f-droid.org/packages/org.kde.kdeconnect_tp/) all of your devices to easily talk to one another when connected to your home network. Easily send files, photos, clipboard data across all of your devices (even on iOS!). KDE connect can be downloaded from F-Droid.
- [Notesnook](https://f-droid.org/en/packages/com.streetwriters.notesnook/) is an E2EE notes application for syncing your thoughts and to-do lists across all of your devices. Their free plan should cover most personal use cases. Notesnook is available on F-Droid.
- [Standard Notes](https://f-droid.org/en/packages/com.standardnotes/) is very similar to Notesnook, but requires a paid plan to match the feature set. Standard Notes is available through F-Droid.
- [Anysoft Keyboard](https://f-droid.org/packages/com.menny.android.anysoftkeyboard/) is a keyboard app that allows you to customize pretty much anything you can think of when it comes to your phone typing experience. It can be downloaded via F-Droid.
- [GBoard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin&hl=en&gl=US) is the default Google keyboard app. In my experience it offers by far the best type and swipe experience. If you download this app, ensure you completely disable all network related permissions. It can be downloaded via Aurora.

![image](assets/17.webp)

Left: Notesnook
Right: KDE Connect

### Lifestyle

- [Geometric Weather](https://f-droid.org/en/packages/wangdaye.com.geometricweather/) is a beautifully designed Open Source weather app available via F-Droid. It also supports may different sizes of widgets so you can see the weather in your chosen location straight from your home screen.
- [Translate You](https://f-droid.org/packages/com.bnyro.translate/) is an Open Source and privacy preserving translation app that supports more than 200 languages. Translate You is available via F-Droid.
- [Proton Calendar](https://proton.me/calendar/download) is a simple to use E2EE that interacts seamlessly with your Proton email accounts. Proton Calendar can be downloaded as an APK or via the Aurora store.
- [PassAndroid](https://f-droid.org/en/packages/org.ligi.passandroid/) is an app for displaying and storing boarding passes, coupons, movie tickets and membership cards etc. Simply download the relevant `pkpass` or `espass` file and open with the app. PassAndroid is available via F-Droid.

![image](assets/19.webp)
Left: Geometric Weather
Right: Proton Calendar

### Security/Privacy

- [Bitwarden](https://mobileapp.bitwarden.com/fdroid/) offers a free and E2EE cross platform password manager solution for all of your devices. Their paid service allows you to integrate 2FA codes into the app. The server side of Bitwarden can be self hosted and the Android app is available via F-Droid.
- [Proton Pass](https://proton.me/pass/download) offers a similar free service to Bitwarden, but [Proton Unlimited](https://proton.me/pricing) customers are able to access additional advanced features. Proton Pass is available via APK or Aurora.
- [FreeOTP](https://f-droid.org/packages/org.fedorahosted.freeotp/) is a two-factor authentication application for systems utilizing one-time password protocols. Tokens can be added easily by scanning a QR code. FreeOTP is available via F-Droid.
- [Aegis](https://f-droid.org/en/packages/com.beemdevelopment.aegis/) is a free, secure and Open Source app for Android to manage your 2-step verification tokens for your online services. Aegis is available via F-Droid.
- [Cryptomator](https://f-droid.org/en/packages/org.cryptomator.lite/) is a paid, cross platform service that encrypts your data locally so you can safely upload it to your favourite cloud service. Cryptomator can be downloaded via F-Droid.

![image](assets/21.webp)
Left: Proton Pass
Right: Bitwarden

### Cloud Solutions

- [Proton Drive](https://proton.me/drive/download) is a paid E2EE cloud solution for backing up and storing all of your files. At the time of writing, they have just announced a Windows desktop client, but Mac and Linux users must continue to use the web version to sync from their computers (for now). The Android client is available as an APK or via Aurora.
- [Skiff](https://skiff.com/download) also offers paid E2EE cloud storage and file collaboration tools. They offer a Mac and Windows desktop client (as well as a web app) and their Android clients must be downloaded from Aurora.
- [Nextcloud](https://f-droid.org/en/packages/com.nextcloud.client/) offers a fully featured cloud based solution for collaboration, cross device sync and file storage. More advanced users can choose to self-host their Free and Open Source software on any hardware they like. The Android clients can be downloaded via F-Droid.
- [Cryptpad](https://cryptpad.fr/) offers a free, web based, E2EE alternative to Google Docs.

![image](assets/23.webp)

Proton Drive

## The Downsides

The Open Source and privacy preserving alternatives to the tech conglomerate applications you've gotten used to using are plentiful, and some of them are often better than the closed source, spyware ridden alternatives.

However when moving to GrapheneOS, there are some creature comforts that you must give up due to no alternatives. These include:

- **Apple CarPlay/Android Auto** - You're going to need to stick to good old fashioned Bluetooth, USB or Aux.
- **Apple/Google Pay** - Pretty much everyone carries their wallet with them anyway!
- **Banking apps** - It's not that these don't work at all. Some do, perfectly in fact. Others work only with Google Play Services enabled (read more on that below) and others just don't work at all. Read the report on your bank [here](https://privsec.dev/posts/android/banking-applications-compatibility-with-grapheneos/) to see the current state of play. Fear not if yours is on the list that does not work, remember you can just save the URL as a web app on your home screen.
- **Push Notifications** - Most applications that send you updates when not using a specific app will do so through Google Play Services. These are not installed by default with GrapheneOS, so if you find yourself not being notified immediately when your friend sends you an email, this is likely why. The good news is that some of the apps mentioned above have implemented their own background connection to periodically check for updates and then give you a notification where required

### Sandboxed Google Play

> 'GrapheneOS has a compatibility layer providing the option to install and use the official releases of Google Play in the standard app sandbox. Google Play receives absolutely no special access or privileges on GrapheneOS as opposed to bypassing the app sandbox and receiving a massive amount of highly privileged access.'

If you find you simply cannot live without those push notifications for your favorite app or a certain 'must have' app is useless without Play Services, GrapheneOS allows you to [install](https://grapheneos.org/usage#sandboxed-google-play-installation) these services in a completely sandboxed environment. Once installed, these services require no Google account to work, and each one's permissions can be tightly controlled.

Before you rush to install these on day 1, I urge you to see how far you get without them. You'll probably be surprised at just how many apps function perfectly normally without.

If you do want to install them, simply tap the pre-installed 'Apps' application followed by 'Google Play Services'. Consider installing them alongside those less private apps you can't live without, inside a completely separate user profile to provide that extra layer of segregation from the rest of your phone.

![image](assets/24.webp)

Play Services install screen

### Profiles

GrapheneOS allows you to have a separate phone experience, within your phone. Additional profiles can install their own apps and services and cannot access any files or data from the owner account.
If you only have one or two of those must have apps that require Play Services, but are only used very infrequently, installing those alongside Play Services in a separate profile might be a great idea to further bolster any minute privacy implications that are left by having them running in the owner profile.

You can read more about this use case [here](https://discuss.grapheneos.org/d/168-ideas-for-user-profiles/2).

If you decide to add a separate profile to suit your use case, the app [Insular](https://f-droid.org/en/packages/com.oasisfeng.island.fdroid/) might be useful to you. Insular allows you to easily clone any of your existing apps across to the new profile without the need to go via any of the traditional install routes covered earlier in this guide. Insular also allows you to quickly 'freeze' any of those apps to completely disable all of that app's background services from running.

![image](assets/24.webp)

User profile management screen

### e-Sims

If you want to take your phone privacy to the next level and have a cell service that is detached from your real world identity, an eSIM might be for you. An eSIM is a virtual SIM that you can purchase online and add to your phone via a QR code. Companies offering such services that can be paid for anonymously with Bitcoin include [Silent.Link](https://silent.link/) and [Bitrefill](https://www.bitrefill.com/gb/en/esims/).

eSIMs should not be looked at as a complete panacea for phone privacy. They can be a useful tool when in the right hands, but please do your research on the [tradeoffs](https://grapheneos.org/faq#cellular-tracking) of using any type of cell service if you intentions is to go completely 'off grid'.

Sandboxed Play Services must be installed for eSIM provisioning in GrapheneOS.

## Backups

After getting your new de-Google'd Pixel phone setup, it's a good idea to create yourself a backup. This backup will enable you to restore the phone to an identical state in the event that you lose your phone or it gets lost/stolen.

You can elect to store the backup file onto any external storage media, or to a self-hosted cloud solution like Nextcloud, although some users report varying levels of success with the latter option.

To create your first backup:

1. Go to **Settings** > **System** > **Backup**, then write down your 12-word recovery code. This code is required to decrypt the backup file at a later date. Lose the code, lose access to your phone backup.
2. Next choose your storage location. I'd recommend an external USB drive or industrial grade microSD card.
3. Choose the data to be backed up. If you have the space on your specified storage medium, I'd advise selecting everything.
4. Tap the three dots n the top right, and choose **Backup now**.

![image](assets/26.webp)

Backup screen

Remember that if you're making offline backups to external storage media, it makes sense to complete this step regularly to ensure any recent important updates to your phone are not lost if the worst were to happen.

![video](https://www.youtube.com/embed/eyWmcItzisk)

Video detailing the backup process

## Conclusion

In recent years the GrapheneOS software has matured significantly. It is more stable and compatible than ever. Coupling this with the flourishing Open Source and privacy preserving app ecosystem, makes GrapheneOS a truly viable alternative to stock Android or iOS, even for 'normal' people just like you!

Data breaches and dragnet surveillance are so commonplace in today's world that they barely make headlines anymore. It's up to you to protect yourself. There will be adjustments and sacrifices to be made along the way, but reducing your exposure to such infringements is nowhere near as difficult as you think it will be.

I hope this guide goes some way to helping you along your journey. If you found this guide useful and would like to support my work, please consider sending a [donation](/tips).

If you are an existing GrapheneOS user, or become one as a result of this guide, consider [donating](https://grapheneos.org/donate) to support their important work.

### Learn more

GrapheneOS is a rabbit hole anyone could easily spend weeks going down. There's just so much you can learn and tinker with to tailor the experience to your requirements and threat models. Below are some links where you can continue your journey:

- [GrapheneOS Official Usage Guide](https://grapheneos.org/usage) - Official Website
- [GrapheneOS Forum](https://discuss.grapheneos.org/) - Official Website
- [GrapheneOS Settings Masterclass](https://www.youtube.com/watch?app=desktop&v=GLJyD9MJgIQ) - Video by 'The Privacy Wayfinder'
- [GrapheneOS General Podcast](https://www.youtube.com/watch?app=desktop&v=UCPX0mFFRNA) - Podcast by 'Watchman Privacy'

full credit to : https://github.com/BitcoinQnA/Bitcoiner.Guide/blob/main/grapheneos.md
